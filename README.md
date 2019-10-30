
# 欢迎使用 「72EX」 API 文档

**72EX 是一个加密货币综合应用平台。
72EX 和根据 72EX 发行的 App 由 Nemoia Global Ltd. 及 Nemoia Capital 全资拥有和经营**


![72EX](https://www.72ex.io/logo.png "72EX")


[72EX（WWW.72EX.IO）](https://www.72ex.io)是一家注册于塞舌尔的加密货币综合应用平台，由Nemoia Global Ltd全资控股经营，Company Number：215264 72EX的技术团队由新加坡、美国、中国等多个国家的专业人才组成，在美国硅谷和新加坡均设有运营点。除此之外，我们还在美国设立了风投基金Nemoia Capital。

72EX作为全球首个跨界交易所，目的不仅仅是作为一个交易媒介，将重点打造加密货币综合应用平台，涵盖游戏娱乐、应用分发、现货期货交易等业务。


---




### 公共响应数据：
					
|参数名称   |是否必须   |类型     |描述     |默认值     |取值范围   |
|---       |:---:     |:---:   |:-----   |-----     |-----     |
|code      |true      |String  |状态码    |　       |200，500，…… |
|message   |true      |String  |状态信息  |　       |SUCCESS，FAILED，…… |
|data      |true      |Object  |返回数据  |　       |SUCCESS，FAILED，…… |


---




## 用户模块

#### 接口列表：

|#      |接口     |说明     |
|:---:  |:---    |:---     |
|1      |```POST /uc/api/v1/asset/wallet```|[钱包信息](./docs/user.md)|


---




## 交易模块

#### 接口列表：

|#      |接口     |说明     |
|:---:  |:---    |:---     |
|1      |```POST /exange/api/v1/order/add```                |[添加委托](./docs/exchange.md)|
|2      |```POST /exange/api/v1/order/history```            |[历史委托](./docs/exchange.md)|
|3      |```POST /exange/api/v1/order/current```            |[当前委托](./docs/exchange.md)|
|4      |```POST /exange/api/v1/order/cancel/{orderId}```   |[取消委托](./docs/exchange.md)|




### End