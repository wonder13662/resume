# ๐งFE ๊ฐ๋ฐ ์ปจ๋ฒค์ ์ด์
# #1 ๋ฐฐ๊ฒฝ

- ์ฝ๋ ๋ฆฌ๋ทฐ์๋ง๋ค ์ฌ์ํ ๋ถ๋ถ์ ์ฐจ์ด๋ค์ ๋ํด ๋ง์ถ๊ธฐ ์ํด ์ถ๊ฐ์ ์ธ ๋น์ฉ์ด ๋ฐ์ํ์.
    - ์นด๋ฉ ์ผ์ด์ค์ธ๊ฐ, ํ์ค์นผ ์ผ์ด์ค์ธ๊ฐ?
- ๊ธฐ์ ์ ์ธ ์ ํ์ ํด์ผ ํ  ๋, ๋ ๋ค ๋ง๋ ํ๋นํ ๊ฒฐ์ ์ด๊ฑฐ๋ ๋ชํํ ๋ต์ด ์๋ ๊ฒฝ์ฐ, FEํํธ์์ ๋ฐฉํฅ์ ์ ํด ํ๋จ์ ๋น์ฉ์ ์ค์ผ ํ์๊ฐ ์์์
    - Api ํต์ ์ ์คํจ๊ฐ ๋ฐ์ํ๋ฉด ์๋ฌ๋ฅผ ํธ๋ค๋งํ๋ ์์น๋ ์ด๋๊ฐ ๋์ด์ผ ํ๋๊ฐ? View์ธ๊ฐ? Service ๋ ์ด์ด์ธ๊ฐ?

# #2 ๋์

- PR ๋ฆฌ๋ทฐ ํน์ ๋ฐ์ผ๋ฆฌ ์งํ ์งง์ ๋ฏธํ์ ํตํด์ FEํํธ ์ฝ๋ฉ ๊ท์น์ ์ ํด์ผ ํ๋ ๊ฒ์ ์ปจ๋ฒค์ ํ์ด์ง์ ํ๋ณด๋ก ๋ฑ๋กํด๋ .
- ์ฃผ๊ธฐ์ ์ผ๋ก ํ๋ณด๋ก ๋ฑ๋กํด๋ ๋ด์ฉ์ ๋ํด FEํํธ ์ฝ๋ฉ ์ ์ ๊ท์น์ผ๋ก ๊ฒฐ์ ํจ
- ์ด๋ฅผ ์ฝ๋ ์์ฑ ๊ธฐ๋ณธ ๋ฃฐ๋ก ๋ฐ๋ฆ

# #3 ์ฑ๊ณผ

- PR ๋ฆฌ๋ทฐ์ ์ ๋งคํ ๋ถ๋ถ์ ๋ํ ์ง๋ฌธ์ด ์ค์ด๋ฌ. PR ๋ฆฌ๋ทฐ ์๊ฐ์ด ์ถ์๋จ.
- ๊ฐ๋ฐ์ ์ธ ๋ฌธ์ ๋ก ์ํต์ ํ  ๋๋ ๊ณตํต์ ๊ฐ๋๊ณผ ์ฉ์ด๋ฅผ ์ฌ์ฉํ๊ฒ ๋์ด ๊ฒฝ์ ์ ์ธ ์ํต์ด ๊ฐ๋ฅํด์ก์.

---
# #4 ์ฐ์ถ๋ฌผ

# Vue2

## Router

1. Restful Api Url ์ปจ๋ฒค์์ Vue Router url์ ์ ์ฉ
    1. ์ปฌ๋ ์ ๋ฆฌ์์ค
        
        ```jsx
        customers
        ```
        
    2. ์ฑ๊ธํด ๋ฆฌ์์ค
        
        ```jsx
        customers/{customerId}
        ```
        
    3. ๋ฆฌ์์ค๋ sub-collection ๋ฆฌ์์ค๋ฅผ ํฌํจํ  ์ ์๋ค
        
        ```jsx
        customers/{customerId}/accounts
        ```
        
    4. ๊ธด ๋ฌธ์์ด์ด๋, ์ฝํ๊ธฐ ์ด๋ ค์ด ๋ฌธ์์ด์ ๋ํด kebab-case๋ก ๊ฐ๋์ฑ์ ๋์ธ๋ค
        
        ```jsx
        // BAD
        http://api.example.com/inventory-management/managedEntities/{id}/installScriptLocation
        // GOOD
        http://api.example.com/inventory-management/managed-entities/{id}/install-script-location
        ```
        
    5. ์ค์  ์ฌ๋ก
        
        ```jsx
        /requesters // requester ๋ชฉ๋ก ํ์ด์ง
        /requesters/{id} // requester 1๋ช์ ๋ํ ์์ธ ํ์ด์ง
        /requesters/{id}/contract // requester 1๋ช์ ๊ณ์ฝ ์ ๋ณด
        /requesters/{id}/wallet // requester 1๋ช์ wallet
        ```
        
    6. Vue router์ ์ค์ฒฉ router๋ฅผ ์ฌ์ฉํด์ ์ Restful Api convention ๊ตฌ์กฐ๋ฅผ ๋ํ๋ด๋๋ก ํ๋ค.
    7. [๊ด๋ จ ๋ผ์](https://github.com/barogo/leo/pull/3070#pullrequestreview-1077651646)
    8. ์ฐธ๊ณ  ์๋ฃ
        
        [๊น๋ํ URL ํจํด์ ์ํ REST Resource Naming Guide](https://velog.io/@pm1100tm/%EA%B9%94%EB%81%94%ED%95%9C-URL-%ED%8C%A8%ED%84%B4%EC%9D%84-%EC%9C%84%ED%95%9C-REST-Resource-Naming-Guide)
        
        [Use RESTful service URLs - API Design Guide 0.1 documentation](https://apiguide.readthedocs.io/en/latest/build_and_publish/use_RESTful_urls.html)
        
2. ~~(depreacted)์ค์ฒฉ ๋ผ์ฐํธ(Nested Router)๋ฅผ ์ฌ์ฉํ์ง ์๋ ์ด์  [๊ด๋ จ๋ผ์](https://github.com/barogo/leo/pull/3070#issuecomment-1216212756)~~
    1. ๊ฐ๋์ฑ๊ณผ ์ ์ง๋ณด์์ ์ด์ 
        1. View์ ๊ตฌ์กฐ์ Router ๊ตฌ์กฐ๋ฅผ ์ต๋ํ ์ ์ฌํ๊ฒ ๋ง์ถ์ด ๊ฐ๋์ฑ์ ๋์๋๋ค.
    2. ์ค์ฒฉ๊ตฌ์กฐ๋ ์ธ์์ ์ด๋ ค์
        1. ๋ฐ์ดํฐ์ ์ฑ๊ฒฉ์ด ์ค์ฒฉ์ ๋ํ๋ด์ผ ํ๋ ์ํฉ์ด ์๋๋ผ๋ฉด ์ต๋ํ ์ค์ฒฉ ํํ์ ๋ฐฐ์ฌํ๋ ๊ฒ์ด ํ์ฌ์ ๋ฐฉํฅ์ฑ์๋๋ค.
    3. ์ฌ์ฉํ์ง ์๊ฒ ๋ ์ด์ 
        1. [Restful Api Url ์ปจ๋ฒค์์ Vue Router url์ ์ ์ฉ](https://www.notion.so/ad83c5e8927142a189926edde3b4c83f) ์ ์ฌ์ฉํ๊ธฐ๋ก ํ๊ธฐ ๋๋ฌธ
3. ~~(deprecated)`requester/requester-list`์ฒ๋ผ ๋ฐ๋ณต๋๋ ๋ค์ด๋ฐ ํ์์ ์ด์  [๊ด๋ จ๋ผ์](https://github.com/barogo/leo/pull/3070#issuecomment-1216212756)~~
    1. ํด๋น View component๋ฅผ ๋น ๋ฅด๊ฒ ๊ฒ์ํ๊ธฐ ์ํ ๋ค์ด๋ฐ์๋๋ค. ๋ง์ผย `requester/list`๋ก router๋ฅผ ์ก๋๋ค๋ฉด, View component๋ ์ด์ ์ผ์นํ๋ย `requester/list.vue`๋ก ์์ฑํ๊ฒ ๋ฉ๋๋ค. ์ด ๊ฒฝ์ฐ, list.vue๋ย `notice/list.vue`,ย `delivery/list.vue`์ฒ๋ผ ์ค๋ณต๋๋ ๊ฒ์ ๊ฒฐ๊ณผ๋ฅผ ๋ธ์ถํ  ์ ์์ผ๋ฏ๋ก ์ํ๋ ๊ฒฐ๊ณผ๋ฅผ ์ฐพ๋๋ฐ ๋ฐฉํด๊ฐ ๋ฉ๋๋ค. ๊ทธ๋ฌ๋ฏ๋ก ๊ฒ์์ ์ด์ ์ ์ํด 2๊ฐ ์ด์์ ๋จ์ด๋ก ๊ณ ์ ์ฑ์ ๋ํ๋ผ ์ ์๋ ๋ค์ด๋ฐ์ ์ ํํ๊ฒ ๋์์ต๋๋ค. ์์ธ๋ฌย [Vue style guide:Tightly coupled component names](https://v2.vuejs.org/v2/style-guide/?redirect=true#Tightly-coupled-component-names-strongly-recommended)๋ฅผ ๋ฐ์ํ ์ธก๋ฉด๋ ์์ต๋๋ค.
    2. ์ฌ์ฉํ์ง ์๊ฒ ๋ ์ด์ 
        1. [Restful Api Url ์ปจ๋ฒค์์ Vue Router url์ ์ ์ฉ](https://www.notion.so/ad83c5e8927142a189926edde3b4c83f) ์ ์ฌ์ฉํ๊ธฐ๋ก ํ๊ธฐ ๋๋ฌธ

## Naming

1. ์ด๋ฒคํธ๋ฆฌ์ค๋: `on${EventName}${TargetName}`
    
    ```html
    <template>
    	<MyComponent
    		@click="onClickMyComponent"
    	/>
    </template>
    <script>
    export default {
    	...
    	methods: {
    		onClickMyComponent() {
    			// do something
    		},
    	},
    };
    </script>
    ```
    

## Vuex

1. ์ปดํฌ๋ํธ ๋ด์ store.dispatch์ ํธ์ถ์ ๋ฉ์๋๋ก ๊ฐ์ธ๋ ๊ฒ์ 2ํ ์ด์ ๋ฐ๋ณต๋๋ ๊ฒฝ์ฐ๋ฅผ ๊ธฐ์ค์ผ๋ก ํ๋ค. 
    1. ์ด์ 
        1. action์ ์ด๋ฆ์ ๋ฌธ์์ด๋ก ์ง์  ๋ณด๋์ผ๋ก ๋ฐ์ํ๋ ์คํ๋ฅผ ๋ง๊ธฐ ์ํจ
        2. ์ฝ๋์ ๊ฐ๊ฒฐ์ฑ๋ ์ด์ ์ด ์์
    2. ์์ ์ฝ๋
        
        ```jsx
        <script>
        export default {
        	...
        	methods: {
        		async onChangePage() {
        			await this.fetchHQWalletStatement();
        		},
        		async onClickMyComponent() {
        			await this.$store.dispatch('hqWallet/fetchHQWalletMoneyTransaction');
        			await this.fetchHQWalletStatement();
        		},
        		async fetchHQWalletStatement() {
        			this.$store.dispatch('hqWallet/fetchHQWalletStatement');
        		},
        	},
        };
        </script>
        
        ```
        
2. Action์ Api ์๋ต์ผ๋ก ๋ฐ์ ์์ฑ ์ค ๋ฐฐ์ด์ด ๊ฐ๊ณตํ๊ฑฐ๋ ์กฐํํ  ๋์์ด๋ผ๋ฉด ๋ฌด์กฐ๊ฑด null ๊ฒ์ฌํด์ ๋น๋ฐฐ์ด๋ก ์ด๊ธฐํ
    1. ์ฌ๋ก: https://github.com/barogo/leo/pull/3240/files
        
        ```jsx
        if (!utils.isValidArray(recommendBlackDrivers)) {
              recommendBlackDrivers = [];
            }
        
            recommendBlackDrivers = recommendBlackDrivers.map((v) => {
              const {
                Driver: {
                  ShippingSubDeliveries,
                },
              } = v;
              if (!utils.isValidArray(ShippingSubDeliveries)) {
                return {
                  ...v,
                  Driver: {
                    ...v.Driver,
                    ShippingSubDeliveries: [],
                  },
                };
              }
              return v;
            });
        ```
        
3. State์ ๋ฐฐ์ด ๊ฐ ์ํ ๊ด๋ฆฌ
    1. api ๊ฒฐ๊ณผ ๋ฐ๊ธฐ ์ : null
    2. api ๊ฒฐ๊ณผ ๋ฐ์ ํ(๊ฒฐ๊ณผ๊ฐ ์๋ค๋ฉด): [](null๋ก ๋ค์ด์๋ ํด๋ผ์ด์ธํธ์์ ๋น ๋ฐฐ์ด๋ก ์ฒ๋ฆฌํด์ ์ ์งํ  ๊ฒ!)
    3. api ๊ฒฐ๊ณผ ๋ฐ์ ํ(๊ฒฐ๊ณผ๊ฐ ์๋ค๋ฉด): [{...}, {...}]
4. Action ๋ ์ด์ด์ parameter์ ๋ํ ๊ฒ์ฆ(validation)
    1. parameter์ ๋ํ ๊ฒ์ฆ์ ํ์ง ์์. parameter์ ๊ฒ์ฆ์ view component์์ `store.dispatch` ์์ ์ ํ๋ ๊ฒ์ผ๋ก ํ์ํจ
    2. ๊ฒ์ฆํ์ง ์๋ ์ด์ 
        1. actions์์ validation์ด ์ถ๊ฐ๋๋ฉด, view component์ ์ค๋ณต๋๋ ๊ฒฝ์ฐ๊ฐ ์๊น. ํจ์จ์ ์ผ๋ก view component ํ ๊ณณ์์๋ง ๊ฒ์ฆ์ ์งํํ๋๋ก ํ์.
    3. ๋ช๋ช ๊ฒฝ์ฐ์ ๋ํด์ actions์์ ๋ฐ๋ parameter์ ๋ํด์ ๊ฒ์ฆ(validaiton)์ ํ์ํ๋ค๊ณ  ๋ณด๋ ๊ฒฝ์ฐ๊ฐ ์์์. view component์ actions๋ ๋ณ๋์ ๋ชจ๋์ด๋ผ๊ณ  ๋ณด๋ ๊ด์ ์ด๋ผ๋ ์ด ์ด์ผ๊ธฐ๊ฐ ํ๋นํจ. ํ์ง๋ง ์์ ์ด์ ๋ค๋ก ๊ฒ์ฆ์ ํ ๊ณณ(view component)์์๋ง ํ๋ ๊ฒ์ผ๋ก ์ ์.
5. Socket์ ์ด๋ฒคํธ ํ๋ฆ (Socket(event.on) โ store.dispatch(service ํฌํจ) โ store โ views)
    
    ```jsx
    const socketClient = {
    	onReceiveMsgGrabSubDelivery(msg) {
    		// 1. ์์ผ ์๋ฒ๋ก๋ถํฐ ๋ฉ์์ง๋ฅผ ๋ฐ์ต๋๋ค.
    		store.dispatch('updateSubDeliveryBySocket', msg)
    	}
    }
    
    const store = {
    	actions: {
    		updateSubDeliveryBySocket(msg) {
    			// 2. socket client์์ ๋ฐ์ ๋ฉ์์ง์ฒ๋ฆฌ
    			const {
    				subDelivery,
    			} = msg;
    
    			// 2-1. resourceWatcher์์ ์ฌ์ฉ์ค์ธ ๋ฆฌ์์ค๋ค๋ง ์๋ฐ์ดํธํ๋๋ก ์กฐ๊ฑด ๊ฒ์ฌ
    			if (resourceWatcher.has(RESOURCE_DELIVERY)) {
    				// 2-1-1. ์ฌ๊ธฐ์ ์ ์ฒ๋ฆฌ ๋จ๊ณ๊ฐ ๋ค์ด๊ฐ ์ ์์ต๋๋ค.
    				// 2-1-2. service์์ ์ ๋ฌ๋ฐ์ subDelivery ๋ด์ฉ์ผ๋ก ์๋ฐ์ดํธ
    				COMMIT(UPDATE_SUBDELIVERY, subDelivery);
    				// 2-1-2. ์ฌ๊ธฐ์ ํ์ฒ๋ฆฌ ๋จ๊ณ๊ฐ ๋ค์ด๊ฐ ์ ์์ต๋๋ค.
    			}
    
    			// 2-2. ์ฌ๊ธฐ์ ํ์ํ๋ค๋ฉด service๋ฅผ ํธ์ถํ  ์ ์์ต๋๋ค.(service ํฌํจ)
    			const result = someService.fetchList();
    			COMMIT(UPDATE_SOMETHING, result);
    		}
    	},
    	getters: {
    		subDelivery(state) {
    			return state.subDelivery;
    		}
    	}
    }
    
    const component = {
    	computed: {
    		subDelivery() {
    			// 3. ์ต์  subDelivery๋ฅผ store์ ๊ฐ์ ธ์ ์ปดํฌ๋ํธ์ ํ์ํฉ๋๋ค.
    			return store.getters['subDelivery'];
    		}
    	}
    }
    ```
    

## Base Component

1. BaseTextArea
    1. ๋นํ์ฑํ ์ค์ ์ disabled๊ฐ ์๋ readonly๋ฅผ ์ฌ์ฉํ์
        1. ์ด์ : disabled๋ ์คํฌ๋กค์ด ๋ถ๊ฐํด์ textarea ์์ญ ๋ฐ๊นฅ์ ๋ด์ฉ์ ๋ณผ ์ ์์. readonly๋ ์คํฌ๋กค ๊ฐ๋ฅ.
2. (ํ๋ณด)Base Component์ ์ญํ ์ ๋ฐ๋ผ atom, molecules, organisms, template, page๋ก ๊ตฌ๋ถ
    
    [Scalable Frontend Component: Atomic Design](https://medium.com/@justarya/scalable-frontend-component-atomic-design-851dd29aa01f)
    
    *BaseComponent์์ ์๋ฃ ๋ค ์ต์ข ๊ฒฐ์ 
    

## Mixins

1. view๋จ์๋ก ํ์ผ ์์ฑ(์ด๋ฆ๋ ๋์ผํ๊ฒ ์ฌ์ฉ)
2. mixin๊ณผ ํด๋น ์ปดํฌ๋ํธ๋ฅผ ์๋ณํ๊ธฐ ์ํด mixin[ํ์ผ๋ช][name] ์ปจ๋ฒค์์ ์ ์ฉ
- ์์

```jsx
// src/mixins/notice.js

//...

export default {
  methods: {
    mixinNoticeCategoryReadable(category) {
      if (!NOTICE__CATEGORY_SET.has(category)) {
        return VALUE_EMPTY;
      }
      return this.$t(`models.notice.NoticeCategoryEnum.${category}`);
    },
    mixinNoticePushPlanOption(pushPlanOption) {
      if (!NOTICE__TARGET_PUSHPLAN_OPTION_ENUM_SET.has(pushPlanOption)) {
        return VALUE_EMPTY;
      }
      return this.$t(`models.notice.NoticeTargetPushPlanOptionEnum.${pushPlanOption}`);
    },
  },
};

// src/views/director/notice/index.vue

//...

const messageTargetReadable = messageTargets.length > 0 ? messageTargets.join(',') : this.mixinCommonValueEmpty();
const pushMessageYesOrNotReadable = this.mixinCommonValueYesOrNo(PushPlan);
const categoryReadable = this.mixinNoticeCategoryReadable(category);
const createdAtReadable = utils.convertUTCToLocalYYYYMMDDHHmmss(createdAt);

//...
```

# Graphql

- ServiceLayer์ query, mutation ์ธ์๋ ์๋ฒ์ฝ๋์ ์ค์ ํ ํ์์ ์ด๋ฆ์ ๊ทธ๋๋ก ์ฌ์ฉํ๋ค.
    - ์ด์ : ๊ฐ๋์ฑ๊ณผ ๊ฒ์์ ํธ์์ฑ์ ๋์ด๊ธฐ ์ํจ
        
        ```jsx
        
        // app/presenter/src/graphql/schemas/pushPlan.graphql
        type Mutation {
          """
          ํธ์์๋ฆผ ์์ฑ
          | ์๋ฌ ์นดํ๊ณ ๋ฆฌ (category) | ์๋ฌ ์ฝ๋ (errorCode) | ์ค๋ช |
          | ------ | ------ | ------ |
          | NOT_FOUND | NOT_FOUND_RESOURCE | ์กฐ๊ฑด์ ์ผ์นํ๋ ๊ฐ์ ์ฐพ์ ์ ์๋ ๊ฒฝ์ฐ |
          | CONFLICT | DUPLICATED_ID | ์ด๋ฏธ ๊ธฐ์กด์ ์์ฒญํ ๊ฒฝ์ฐ |
          """
          createPushPlan(input: CreatePushPlanData!): PushPlan
        }
        
        input **CreatePushPlanData** {
          "notice ID"
          noticeId: ID
          "ํธ์์๋ฆผ ๋ณธ๋ฌธ"
          contents: String!
          "ํธ์์๋ฆผ ๋๋ผ์ด๋ฒ ๋์ ์ฌ๋ถ"
          targetDriverFlag: Boolean!
          "ํธ์์๋ฆผ ๋๋ ํฐ ๋์์ฌ๋ถ"
          targetDirectorFlag: Boolean!
          "๋ฉ์์ง ๋ฐ์ ์ง์ญ ์ ์ฒด ์ฌ๋ถ"
          isTargetingAllPhysicalGroup: Boolean!
          "ํธ์ ์ด๋ฒคํธ๊ฐ ์์๋๋ ๋ ์ง"
          pushEventsBeginsAt: DateTime!
          "ํธ์ ์ด๋ฒคํธ๊ฐ ์ข๋ฃ๋๋ ๋ ์ง"
          pushEventsEndsAt: DateTime!
          "ํธ์์๋ฆผ ๋ฐ์ physicalGroup ID ๋ชฉ๋ก"
          physicalGroupIds: [ID]
          "ํธ์์๋ฆผ ์ด๋ฒคํธ ์๊ฐ"
          eventAtHHmmList: [Time!]!
        }
        
        // src/services/graphql/pushPlan.js
        async createPushPlan({
            **CreatePushPlanData**: { // ์ฌ๊ธฐ์ ์ด๋ฆ์ ๊ทธ๋๋ก ๊ฐ์ ธ์ ์ฌ์ฉ
              noticeId,
              contents,
              targetDriverFlag,
              targetDirectorFlag,
              isTargetingAllPhysicalGroup,
              pushEventsBeginsAt,
              pushEventsEndsAt,
              physicalGroupIds,
              eventAtHHmmList,
            },
          }) {
            const { data: result, error } = await apolloClient.getInstance().mutate({
              mutation: createPushPlan,
              variables: {
                input: {
                  ...(noticeId && { noticeId }),
                  contents,
                  targetDriverFlag,
                  targetDirectorFlag,
                  isTargetingAllPhysicalGroup,
                  pushEventsBeginsAt,
                  pushEventsEndsAt,
                  ...(utils.isValidArray(physicalGroupIds) && { physicalGroupIds }),
                  eventAtHHmmList,
                },
              },
            });
        
            if (error) {
              throw error;
            }
        
            return result;
          },
        ```
        
- graphql CRUD ๋ฉ์๋์ ๋ค์ด๋ฐ
    - ๊ฒฐ๋ก : ๋ช์์ ์ผ๋ก ํํํ๋ ๋ฐฉ์์ ์ฐ์
    - fetchOne vs fecthNotice
        
        ```jsx
        // Bad
        services.graphql.notice.fetchOne();
        // Good
        services.graphql.notice.fecthNotice();
        ```
        
    - fetchList vs fetchNoticeList
        
        ```jsx
        services.graphql.notice.fetchList();
        services.graphql.notice.fetchNoticeList();
        ```
        
    - create vs createOne vs createNotice
        
        ```jsx
        services.graphql.notice.create();
        services.graphql.notice.createOne();
        services.graphql.notice.createNotice();
        
        services.graphql.notice.createMoneyTransactionDetails();
        services.graphql.notice.createOptionFeeWithRequestHistory();
        ```
        
    - update vs updateOne vs updateNotice
        
        ```jsx
        services.graphql.notice.update();
        services.graphql.notice.updateOne();
        services.graphql.notice.updateNotice();
        ```
        
- Create, Update ์ดํ์ Read๋ฅผ ๋ค์ ํ๋ ๋์์ View Component์์ ์ํํ๋ค. Action ๋จ์์ ์ฐ์์ผ๋ก ํธ์ถํ์ง ์๋๋ค.
    - ์ด์ :
        - Create์ Read๊ฐ ๊ฐํ๊ฒ ์์กด์ฑ์ ๊ฐ์ง๋ฉด ์ ์ฐ์ฑ์ด ๋จ์ด์ง.
        - action ์์์๋ 1๊ฐ์ ๊ธฐ๋ฅ๋ง ๋์ํ๊ฒ ํ์(SRP:๋จ์ผ์ฑ์์์น)
    
    ```jsx
    // Bad
    // Vuex.action 
    async fetchList() {
    	await services.graphql.notice.fetchList();
    }
    async createNotice() {
    	await services.graphql.notice.createNotice();
    	await dispatch('fetchList', {});
    }
    
    // Good
    // View component
    methods: {
    	async onSubmit() {
    		await this.$store.dispatch('notice/createNotice');
    		await this.$store.dispatch('notice/fetchList');
    	}
    },
    
    // Vuex.action 
    async fetchList() {
    	await services.graphql.notice.fetchList();
    }
    async createNotice() {
    	await services.graphql.notice.createNotice();
    }
    ```
    

# Constant(์์)

1. ์ด๋ค ๊ฐ๋์ ์์ฑ์ ๋ํ๋ผ ๋,ย `${๊ฐ๋}__${์์ฑ}`์ ์ปจ๋ฒค์์ ์ฌ์ฉํ๋ค [๊ด๋ จ ๋ผ์](https://github.com/barogo/leo/pull/3353#discussion_r963384624)
    
    ```html
    DELIVERY_EVENT__ROLE_SET
    ```
    
2. graphql์ enum ๊ฐ์ ์๋ฒ์ ํํ์ ๋ฐ๋ฅธ๋ค. ํ์ฌ๋ [PascalCase](https://namu.wiki/w/%EC%BD%94%EB%94%A9%20%EC%8A%A4%ED%83%80%EC%9D%BC#s-3.2)๋ฅผ ์ฐ๊ณ  ์์. ์ด๋ i18n์๋ ๋์ผํ๊ฒ ์ ์ฉ๋๋ค.
    
    ```graphql
    enum RequesterContractOptionFeeTypeRateTypeEnum {
      deliveryFee
      distance
      fixed
      productPriceCompensation
    }
    ```
    
3. ํด๋ผ์ด์ธํธ ๋ด๋ถ์์ ์ ์ํ ์์๋ [snake_case](https://namu.wiki/w/%EC%BD%94%EB%94%A9%20%EC%8A%A4%ED%83%80%EC%9D%BC#s-3.3) + UPPER_CASE๋ก ํํํ๋ค. ๋ฌธ์์ด ๊ฐ๋ ๋์ผํ ์ปจ๋ฒค์์ผ๋ก ์์ฑ. ์ด๋ i18n์๋ ๋์ผํ๊ฒ ์ ์ฉ๋๋ค.
    
    ```jsx
    PAGINATION_LIMIT_SMALL: 5,
    PAGINATION_LIMIT_DEFAULT: 10,
    PAGINATION_LIMIT_LARGE: 1000,
    PAGINATION_CURRENT_PAGE_DEFAULT: 1,
    
    PAGE_MODE: {
      DIRECTOR_GROUP_READ: 'DIRECTOR_GROUP_READ',
      DIRECTOR_GROUP_CREATE: 'DIRECTOR_GROUP_CREATE',
      DIRECTOR_GROUP_UPDATE: 'DIRECTOR_GROUP_UPDATE',
    },
    ```
    

## ์กฐ๊ฑด๋ฌธ

- ์ผํญ ์ฐ์ฐ์๋ณด๋ค if-return์ ์ฌ์ฉํ๋ค.

```jsx
// Bad
const mixinDeliveryStatusReadable = (deliveryStatus) => {
	return DELIVERY_STATUS_SET.has(deliveryStatus) ? this.$t(`models.delivery.DeliveryStatusEnum.${deliveryStatus}`) : valueEmpty
}

// Good
const mixinDeliveryStatusReadable = (deliveryStatus) => {
  if (!DELIVERY_STATUS_SET.has(deliveryStatus)) {
    return valueEmpty;
  }
  return this.$t(`models.delivery.DeliveryStatusEnum.${deliveryStatus}`);
}
```

# Code Review

1. ์์ ์ฌํญ ํ์ธ์ด ์๋ฃ๋ ๊ฒ์ ํ์ธํ์๋๋ ๋ฐ๋ด๐
    
    ![์์ ํ์ธ์๋ฃ์ ๋ฐ๋ด!](../assets/barogo__frontend_coding_convention_001_code_review_thumbs_up.png)
    
2. ์์ ์ฌํญ์ ๋ํด์ ๋ฐ๋์ ์๋ํ๋ฉด์ ์์์ผ๋ก ๊ธฐ๋กํด์ ์๋ฐ์ดํธํ๋๋ก ํ๋ค.

# Test

## ํ์คํธ ์ฝ๋ ์์ฑ ๋์

- ๊ณต์ฉ ๋ชจ๋ํ๋ ๋ฉ์๋๋ค. ex) utils, mixins
- Vuetify์ input, textarea์ ์ ์ฉ๋๋ rules ๋ก์ง๋ค
    - ์ฌ๋ก: https://github.com/barogo/leo/issues/3933

# UI

- Textarea์ Input์ placeholder๋ก ๋น๊ฐ์ ๋ํ๋ธ๋ค. ์ด ๊ฒฝ์ฐ ๋ธ์ถ๋๋ ๋ฉ์์ง๋ ์๋ ํฌ๋งท์ฒ๋ผ ํ์ํ๋ค.
    
    ```jsx
    placeholder: "${value}๋ฅผ ์๋ ฅํด์ฃผ์ธ์"
    ```
    
- ํ์ด๋ธ ์ปฌ๋ผ์ ์์ ๋น๊ฐ์ โ-โ๋ก ํ์ํ๋ค.

# Error Handling

## try/catch

- Api ํต์ ์ ์ํํ๋ ๋ชจ๋๋จ์์๋ ๋ฐ์ดํฐ์ ๋ํ ์ฒ๋ฆฌ๋ง ๋ด๋นํ๋ค
    
    ```jsx
    // action layer
    // src/store/modules/auth/actions.js
    	async getEmail({ dispatch }, { name, phoneNumber }) {
        try {
          const response = await services.rest.auth.getEmail(name, phoneNumber);
          const { status } = response;
          if (status !== HTTP_RESPONSE_STATUS_CODE.OK_200) {
            // TODO ์๋ฌ ๋ฐ์ดํฐ์ ๊ฐ๊ณต(ํด๋ผ์ด์ธํธ๊ฐ ์ฌ์ฉํ๋ ์๋ฌ์ฝ๋)์ด ํ์ํฉ๋๋ค.
            throw new Error(response?.data?.error);
          }
          return response?.data;
        } catch (error) {
          dispatch('error/addError', error, { root: true });
          throw error;
        }
      },
    ```
    
- Api ํต์  ๊ฒฐ๊ณผ๋ฅผ ๋ฐ์ View ์ปดํฌ๋ํธ ์ชฝ์์ ํ์ํ  ๋ฉ์์ง๋ฅผ ๊ฐ๊ณตํ๋ ์์์ ์ํํ๋ค.
    
    ```jsx
    
    // view layer
    // src/views/auth/FindEmail.vue
    async onClickFindEmail() {
      try {
        // 1. ID ์ฐพ๊ธฐ ์์ฒญ
        const { name, phoneNumber } = this;
        const data = await this.$store.dispatch('auth/getEmail', { name, phoneNumber });
        const { email } = data;
        // 2. ID ์ฐพ๊ธฐ ๊ฒฐ๊ณผํ์ด์ง๋ก ์ด๋
        this.$router.push({
          name: 'FindEmailResult',
          params: {
            email,
          },
        });
      } catch (error) {
        // 3. ID ๊ฒฐ๊ณผ ์ฐพ๊ธฐ ์คํจ. ์คํจ ๋ค์ด์ผ๋ก๊ทธ ๋ธ์ถ
    		// TODO ํด๋ผ์ด์ธํธ ์๋ฌ์ฝ๋์ ๋ฐ๋ฅธ ๋ฉ์์ง ๋งต์ด ํ์ํฉ๋๋ค.
        this.dialog = {
          isShow: true,
          title: this.$t('views.auth.findEmail.dialogFindEmailFailTitle'),
          content: this.$t('views.auth.findEmail.dialogFindEmailFailContent'),
        };
      }
    },
    
    ```
    

### ๊ด๋ จ ๋ผ์

- [PR ๋ฆฌ๋ทฐ #4237](https://github.com/barogo/leo/pull/4237#discussion_r1047156687)

# General(์ผ๋ฐ)

## Import ์์

1. ์ธ๋ถ ๋ชจ๋
2. ์๋น์ค ๊ณต์ฉ ๋ชจ๋
3. ์์ฑํ๋ ์ฝ๋์ ์ธ์ ํ ๋ชจ๋

```jsx
// ์ธ๋ถ ๋ชจ๋
import axios from 'axios';
// ์๋น์ค ๊ณต์ฉ ๋ชจ๋
import BaseSearchTable from '@/components/base/composite/BaseSearchTable';
import BaseButtonXSmall from '@/components/base/BaseButtonXSmall';
import utils from '@/lib/utils';
import {
  COMMON__PAGINATION_CURRENT_PAGE_DEFAULT,
  COMMON__PAGINATION_LIMIT_SMALL,
} from '@/lib/constants';
import mixins from '@/mixins';
// ์์ฑํ๋ ์ฝ๋์ ์ธ์ ํ ๋ชจ๋
import CSTicketDialog from '../components/CSTicketDialog';
```

## Utils

- ์ธ๋ถ ๋ผ์ด๋ธ๋ฌ๋ฆฌ(moment ๋ฑ)์ ๊ฐ๋ฅํํ ์ธ๋ถ๋ก ๋ธ์ถํ์ง ๋ง๊ณ , utils์์ wrappingํด์ ์ฌ์ฉํ๋๋ก ํ์.
- ์์ฃผ ์ฌ์ฉ๋๋ ๊ฒฝ์ฐ(3ํ์ด์)์ ์ธ๋ถ ๋ผ์ด๋ธ๋ฌ๋ฆฌ(ex: moment)์ ๋ํด์ utils๋ก ์ถ๊ฐํ๋ ๊ฒ์ ์งํํฉ๋๋ค. ๊ทธ ์ธ์ ์ํฉ์๋ ์์ ๋กญ๊ฒ ์ฌ์ฉํ๋๋ก ํฉ๋๋ค. [๊ด๋ จ ๋ผ์](https://github.com/barogo/leo/pull/4079#discussion_r1035419838)

## Method Return

- ๋ฉ์๋์ ๋ง์ง๋ง์ ๊ฒฐ๊ณผ๊ฐ์ ๋ฆฌํดํ  ๊ฒฝ์ฐ, ํจ์ ํธ์ถ๊ตฌ๋ฌธ์ ๊ทธ๋๋ก ๋ฆฌํดํ๋ ๊ฒ์ด ์๋ ๊ฒฐ๊ณผ๊ฐ์ ๋ฐ์์ ๋ฆฌํดํ๋ ํํ๋ก ๋ง๋ค์
- ์ด์ 
    - ๋น๋๊ธฐ ํจ์๋ฅผ ํธ์ถํ  ๊ฒฝ์ฐ, Promise๋ฅผ ๋ฆฌํดํ๋๋ฐ ๋๊ธฐํจ์์ฒ๋ผ ์ฒ๋ฆฌํ๋ ๊ฒ์ ๋ง๊ธฐ ์ํจ. ์๋ฌ๋ฌ์๋ ์ฐพ๊ธฐ ๊ณจ์ํ๊ณ  ์์  ์ฒดํฌ๊ฐ ์ ์๋จ.
    - ๋ฆฌํดํ๋ ๊ฒฐ๊ณผ์ ๋ํ ํ์ฒ๋ฆฌ ๋ฑ์ ์ฉ์ดํ๊ฒ ํ๊ธฐ ์ํ ๋ชฉ์ 

```jsx
process(v) {
	// ์ธ์๋ฅผ ๋ฐ์ ์ฒ๋ฆฌํฉ๋๋ค.
  return v + 1;
}
// BAD
doSomting() {
	return process(v);
}
// GOOD
doSomthingBetter() {
	const result = process(v);
	return result; 
}
```

# Data flow

- Flux์ ๊ธฐ๋ณธ ์ฒ ํ์ธ One way data flow(๋จ๋ฐฉํฅ ๋ฐ์ดํฐ ํ๋ฆ)์ ์ค์ํฉ๋๋ค.
    
    [In-Depth Overview | Flux](https://facebook.github.io/flux/docs/in-depth-overview)
    
- ๋ฐ์ดํฐ ์กฐํ๊ฐ ํ์ํ ๊ฒฝ์ฐ(graphql์ ๊ฒฝ์ฐ)
    - Vue component -> @/store/${๋ชจ๋}/Actions -> @/services/${๋ฆฌ์์ค} -> @/lib/graphql/apolloClient ์ ํ๋ฆ์ผ๋ก ์ฐ๊ฒฐ๋ฉ๋๋ค.
