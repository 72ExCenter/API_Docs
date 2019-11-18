
# Welcome to use the "72EX" API documentation

**The 72EX is a comprehensive cryptocurrency application platform. 
72EX and App released under 72EX are wholly owned and operated by Nemoia Global Ltd. and Nemoia Capital.**


![72EX](https://www.72ex.io/logo.png "72EX")


[72EX（WWW.72EX.IO）](https://www.72ex.io)is a comprehensive cryptocurrency application platform registered in Seychelles, which is wholly owned and operated by Nemoia Global Ltd. Company Number: 215264. Its technical team is composed of professionals from Singapore, the United States, China and other countries. It has operations in both US Silicon Valley and Singapore. In addition, we have also set up the Nemoia Capital, a venture capital fund in the United States.

72EX, the world's first cross-border exchange, aims not only to be a trading medium, but also to build a comprehensive application platform for cryptocurrency, covering game entertainment, application distribution, spot futures trading and other businesses.


---
<br>







## Public method

#### Interface list：

|#      |Interface     |Description    |
|:---:  |:---    |:---     |
|1      |```Request and subscription description```|[Request and subscription description](./docs/en-us/common.md#request-and-subscription-description)|
|2      |```API public response data```|[API public response data](./docs/en-us/common.md#api-api-public-response-data)|
|3      |```Signature verification```|[Signature verification](./docs/en-us/common.md#signature-verification)|


---
<br>



## User module

#### Interface list：

|#      |Interface     |Description    |
|:---:  |:---    |:---     |
|1      |```POST /uc/api/v1/asset/wallet```|[Wallet information](./docs/en-us/user.md#post-ucapiv1assetwallet-Wallet-information)|


---
<br>



## Market information module

#### Interface list：

|#      |Interface     |Description    |
|:---:  |:---    |:---     |
|1      |```POST /market/latest-trade```|[Real-time trade data](./docs/en-us/market.md#post-marketlatest-trade-real-time-trade-data)|
|2      |```POST /market/exchange-plate```|[Order book information](./docs/en-us/market.md#post-marketexchange-plate-order-book-information)|

---
<br>



## Trading module

#### Interface list：

|#      |Interface     |Description    |
|:---:  |:---    |:---     |
|1      |```POST /exange/api/v1/order/add```                |[添加委托](./docs/en-us/exchange.md#post-exangeapiv1orderadd-添加委托)|
|2      |```POST /exange/api/v1/order/history```            |[历史委托](./docs/en-us/exchange.md#post-exangeapiv1orderhistory-历史委托)|
|3      |```POST /exange/api/v1/order/current```            |[当前委托](./docs/en-us/exchange.md#post-exangeapiv1ordercurrent-当前委托)|
|4      |```POST /exange/api/v1/order/cancel/{orderId}```   |[取消委托](./docs/en-us/exchange.md#post-exangeapiv1ordercancelorderId-取消委托)|

---
<br>



### End