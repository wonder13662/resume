# 🎲Component test:Jest

# 배경

- BaseComponent 작업으로 자주 사용하는 컴포넌트들이 공통화되면서, 산발적으로 작성되던 테스트 코드들이 패턴을 갖기 시작함
- 이 패턴들을 분석해서 테스트 코드를 재사용할 수 있는 모듈로써 작성하는 작업을 진행하게 됨

# 목적

- 테스트는 이벤트의 발생으로 작성된 변경 데이터가 Api 호출의 매개변수로 반영되었는지 검사하는 것을 기본으로 한다.
- 서버 및 외부 요청은 mocking해서 구현한다.
- 자주 반복되는 테스트 케이스와 환경 구성등은 모듈화해서 재사용 가능하도록 한다.

# 성과

- 기존 수동 테스트 4시간 정도 분량을 1분만에 자동 테스트로 언제든 구동할 수 있게 되었음.
- Vuetify 및 BaseComponent의 테스트 모듈이 작성되어, View 컴포넌트 내의 자식 컴포넌트들이 보일러플레이트 성격의 작업을 통해 이벤트를 일으키거나 데이터를 검증하지 않고, 한번의 메서드 호출(submit)로 변경을 일으켜 테스트 코드를 짧게 구성할 수 있게 되었음.
- BaseSearchTable 등의 공용 모듈의 템플릿에 대해 테스트 케이스를 재사용할 수 있게 되었음.
- 테스트 환경 구성에 대해 캡슐화함으로써 테스트 작성자는 테스트 시나리오에 대해서만 집중할 수 있음.
- 테스트 케이스 재사용으로 복잡한 시나리오의 View 단위로 테스트가 가능해짐으로써 자동으로 반복적인 재귀 테스트가 가능해짐. 어플리케이션의 기능을 보장할 수 있게 됨.
- BaseComponent 리팩토링 시에 기존 기능의 동작을 보장할 수 있음. 리팩토링 안정성이 올라감.

# 구조

### testTools

- baseComponentWrapper
    - BaseComponent에 접근해서 이벤트를 일으키고 내부의 값을 조회하는 기능을 제공합니다.
- testCaseHelper
    - 자주 사용되는 테스트 케이스를 모아둔 모듈입니다.
- vuetifyHelper
    - vuetify의 vue model에 대해 작업을 수행하는 헬퍼 메서드들의 모듈입니다.
- vuetifyWrapper
    - vuetify의 vue model의 참조를 저장해두고 vuetifyHelper의 작업을 수행하게 도와주는 wrapper 입니다.
- baseComponentHelper.js
    - BaseSeacrhTable의 기능을 도와주는 Helper 모듈입니다.
- componentHelper.js
    - Vue class와 컴포넌트가 동일한지 판단하는 헬퍼입니다.
- configManager.js
    - 자주 사용되는 테스트 환경을 재사용할 수 있도록 하는 모듈입니다.
- i18n.js
    - 테스트시의 국제화 처리를 담당하는 모듈입니다.
- index.js
    - 외부에 노출할 메서드를 제어하는 진입점 모듈입니다.
- jestHelper.js
    - jest의 mockFn을 쉽게 사용할 수 있도록 도와주는 모듈. 현재는 Api 호출 메서드를 감싸서 Api 호출시 어떤 payload를 보냈는지 가져오는 역할만 하고 있음.
- testHelper.js
    - 테스트시 필요한 기능을 제공. 현재는 문자열을 원하는 길이만큼 만들어주는 메서드가 있음.

# 적용 범위

### Admin web

- [ ]  admin/account
- [x]  admin/csTicket
- [x]  admin/delivery
- [x]  admin/director
- [x]  admin/driver (50%)
- [x]  admin/feeAdjust (50%)
- [x]  admin/notice
- [x]  admin/physicalGroup (50%)
- [x]  admin/requester (50%)
- [x]  admin/subDelivery

# 테스트 동작 스크린샷

![테스트 스크린샷](../assets/barogo__jest_test_run.gif)

10배속으로 플레이됩니다. 실제 걸린 시간은 약 1분입니다.