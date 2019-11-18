
# 欢迎使用 「72EX」 API 文档

**72EX 是一个加密货币综合应用平台。72EX 和根据 72EX 发行的 App 由 Nemoia Global Ltd. 及 Nemoia Capital 全资拥有和经营**


![72EX](https://www.72ex.io/logo.png "72EX")


[72EX（WWW.72EX.IO）](https://www.72ex.io)是一家注册于塞舌尔的加密货币综合应用平台，由Nemoia Global Ltd全资控股经营，Company Number：215264 72EX的技术团队由新加坡、美国、中国等多个国家的专业人才组成，在美国硅谷和新加坡均设有运营点。除此之外，我们还在美国设立了风投基金Nemoia Capital。

72EX作为全球首个跨界交易所，目的不仅仅是作为一个交易媒介，将重点打造加密货币综合应用平台，涵盖游戏娱乐、应用分发、现货期货交易等业务。


---
<br>







## 公共方法

#### 接口列表：

|#      |接口     |说明     |
|:---:  |:---    |:---     |
|1      |```请求与订阅说明```|[请求与订阅说明](./docs/zh-cn/common.md#请求与订阅说明)|
|2      |```API 公共响应数据```|[API 公共响应数据](./docs/zh-cn/common.md#api-公共响应数据)|
|3      |```验签```|[验签](./docs/zh-cn/common.md#验签)|


---
<br>



## 用户模块

#### 接口列表：

|#      |接口     |说明     |
|:---:  |:---    |:---     |
|1      |```POST /uc/api/v1/asset/wallet```|[钱包信息](./docs/zh-cn/user.md#post-ucapiv1assetwallet-用户钱包信息)|


---
<br>



## 行情模块

#### 接口列表：

|#      |接口     |说明     |
|:---:  |:---    |:---     |
|1      |```POST /market/latest-trade```|[实时成交数据](./docs/zh-cn/market.md#post-marketlatest-trade-实时成交数据)|
|2      |```POST /market/exchange-plate```|[盘口信息](./docs/zh-cn/market.md#post-marketexchange-plate-盘口信息)|

---
<br>



## 交易模块

#### 接口列表：

|#      |接口     |说明     |
|:---:  |:---    |:---     |
|1      |```POST /exange/api/v1/order/add```                |[添加委托](./docs/zh-cn/exchange.md#post-exangeapiv1orderadd-添加委托)|
|2      |```POST /exange/api/v1/order/history```            |[历史委托](./docs/zh-cn/exchange.md#post-exangeapiv1orderhistory-历史委托)|
|3      |```POST /exange/api/v1/order/current```            |[当前委托](./docs/zh-cn/exchange.md#post-exangeapiv1ordercurrent-当前委托)|
|4      |```POST /exange/api/v1/order/cancel/{orderId}```   |[取消委托](./docs/zh-cn/exchange.md#post-exangeapiv1ordercancelorderId-取消委托)|

---
<br>



### End