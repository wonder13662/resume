# ๐๏ธCSํฐ์ผ ํ๋ก์ฐ

# CSํฐ์ผ ์นดํ๊ณ ๋ฆฌ

- ์ผ๋ฐ(normal)
- ๋ฐฐ์ก(delivery)

# ์ผ๋ฐ CSํฐ์ผ ํ์

| ๊ฐ์ | accountRegister |
| --- | --- |
| ํํด | accountWithdrawal |
| ์ด์ก์๋จ | transportation |
| ํ๋์ง์ญ | physicalGroup |
| ๋ฑ๊ธ | grade |
| ๋ณดํ | insurance |
| ์๋ฅ๋ฐ๊ธ | document |
| ์ ์ฐ | feeAdjust |
| ๊ธฐํ | custom |

# ๋ฐฐ์ก CSํฐ์ผ ํ์

| ํฝ์์ง ์ค์ | mistakeByPickupPoint |
| --- | --- |
| ํฌ๋ก์ค ๋ฐฐ์ก | crossDelivery |
| ํฝ์์ง ๋์ฐฉ์ง์ฐ์์ฒญ | pickupDelay |
| ๋ฐฐ์ฐจ๋ฅผ ์ทจ์ํ๊ณ  ์ถ์ด์ | askCancelGrab |
| ์ (๋๋ผ์ด๋ฒ)๊ฐ ์ค์ํ์ด์ | mistakeByDriver |
| ๋ฐฐ์ก์ด ์ทจ์๋์์ด์ | canceledDelivery |
| ๋๋์ง์ ๊ณ ๊ฐ์ด ์์ด์ | notExistCustomerAtDropPoint |
| ๋๋์ง ์ฃผ์๊ฐ ํ๋ ค์ | wrongDropPointAddress |
| ๋๋์ง ๋์ฐฉ์ง์ฐ์์ฒญ | dropDelay |
| ๋ฐฐ์ฐจ์ง์ฐ | delayGrab |
| ๊ธฐํ | custom |

# CSํฐ์ผ ์ฌ์ 

| ์๋ด์ฌ ๋ฌธ์ | custom |
| --- | --- |
| ์ฌ์์๋์์ฒ์ง์ ์์์ฆ ๋ฐ๊ธ | withholdingTaxReceipt |
| ํด์ง์ฌ์คํ์ธ์ | requestAccountWithdrawalDate |
| ์ฑ๊ถํฌ๊ธฐ(๋ฐฐ์ก๋ฃํฌ๊ธฐ) | giveUpDeliveryFee |
| ์ ์ฐ๋ด์ญํ์ธ | requestCompletedFeeAdjust |
| ์ ์ฐ๊ณ์ข๋ณ๊ฒฝ | changeFeeAdjustAccount |
| ํฝ์์ง ์ํ๋๋ฝ | missingProductByPickupPoint |
| ํฝ์์ง ์์์ข๋ฃ | closePickupPoint |
| ํฝ์์ง ์ฃผ์ ์ค๋ฅ | invalidAddress |
| ๊ณผ์  | overload |
| ํฝ์์ง ๋ฏธ์คํจํน | missPackingProduct |
| ํฝ์์ง ์ํํ์ | damagedProductByPickupPoint |
| ๋ฐฐ์ก๋ถ๊ฐ์ํ | impossibleDeliveryProduct |
| ํฌ๋ก์ค ๋ฐฐ์ก | crossDelivery |
| ํญ์ฐ | heavyRain |
| ํญ์ค | heavySnow |
| ๊ฐํ | strongWind |
| ์ฃผ์ฐจ๋ถ๊ฐ/๊ตํต์ฒด์ฆ | trafficJam |
| ๋๋ผ์ด๋ฒ ๋ณ๊ฒฝ | changeDriver |
| ๊ธฐํ | etc |
| ์ด๋์๋จ ๊ณ ์ฅ/์ฃผ์ /๋ฐฐํฐ๋ฆฌ ๋ถ์กฑ | transportationProblem |
| ์กฐ๋ฆฌ์ง์ฐ(๋งค์ฅ๋๊ธฐ) | pickupDelayByPickupPoint |
| ๋๋์ง๊ฑฐ๋ฆฌ | dropPointDistance |
| ํฝ์์ง๊ฑฐ๋ฆฌ | pickupPointDistance |
| ๋ฐฐ์ก ์ค ๊ตํต์ฌ๊ณ  | trafficAccident |
| ์ค๋ฐฐ์ก | missingProductByDriver |
| ๋๋ผ์ด๋ฒ ์ํํ์ | damagedProductByDriver |
| ๋๋ผ์ด๋ฒ ์ํ์ ์ค | lostProduct |
| ๋ฐฐ๋ฌ์ํ๋ณ๊ฒฝ | changeSubDeliveryStatus |
| ๋ฐฐ์ก์ทจ์ | canceledDelivery |
| ๋๋์ง ๊ณ ๊ฐ๋ถ์ฌ | notExistCustomerAtDropPoint |
| ๋๋์ง ์ฃผ์์ค๋ฅ | wrongDropPointAddress |
| ๋๋์ง ๋์ฐฉ์ง์ฐ์์ฒญ | dropDelay |
| ๋ฐฐ์ฐจ์ง์ฐ | delayGrab |

# CSํฐ์ผ ์ํ

| ๋ฑ๋ก | register |
| --- | --- |
| ๋ฐฐ์  | assign |
| ์๋ฃ | done |

# ์๋๋ฆฌ์ค

1. ๋ฐฐ์ก์ค์ธ ๋๋ผ์ด๋ฒ์ ์ฑ์์ ์ด๋ฏธ ํฝ์์ง์ฐ์์ฒญ 5๋ถ์ด ์๋ ๋ฐฐ์ก ๊ด๋ จ CSํฐ์ผ ํ์:โํฝ์์ง ๋์ฐฉ์ง์ฐ ์์ฒญโ์ ์์ฑ. ๊ทธ ๋ค์ ๋๋ ํฐ ์น์์ ์ CS ํฐ์ผ์ ํ์ธํ์ฌ ํ ๋น๋ฐ์
    
    ![๋๋ผ์ด๋ฒ๊ฐ CSํฐ์ผ ๋ฐ๊ธ](../assets/barogo__csticket_001_request.gif)
    
2. ๋๋ ํฐ๊ฐ ๋๋ ํฐ ์น์์ ๋ด์ฉ์ ํ์ธํ๊ณ  ํฝ์์ง ๋์ฐฉ์๊ฐ ์ง์ฐ์ฒ๋ฆฌ๋ฅผ ํจ
    
    ![๋๋ ํฐ๊ฐ ํฝ์์ง์ฐ์๊ฐ ๋๋ฆผ](../assets/barogo__csticket_002_delay_pickup_point_arrive.gif)

    
3. CS ํฐ์ผ์ ๋ฉ๋ชจ-์ด๋ ฅ์ ๋จ๊ธฐ๊ณ  ์๋ฃ์ฒ๋ฆฌํจ
    
    ![๋๋ ํฐ๊ฐ CSํฐ์ผ ์๋ฃ](../assets/barogo__csticket_003_done_csticket.gif)