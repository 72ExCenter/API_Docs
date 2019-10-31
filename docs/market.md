## 用户模块


#### API Reference：

|#      |请求方法     |请求类型    |描述     |验签    |
|:---:  |:---:       |:---:      |:---:    |:---:   |
|1|[POST /market/latest-trade](#post-marketlatesttrade-实时成交数据)|POST|实时成交数据|是|
|2|[POST /market/exchange-plate](#post-marketexchangeplate-盘口信息)|POST|盘口信息|是|

---
<br>



#### POST /market/latest-trade 实时成交数据

#### 请求参数：

|参数名称    |是否必须    |类型    |描述        |默认值     |取值范围    |
|:---       |:---:      |:---:   |:---        |:---      |---        |
|symbol    |true        |String  |交易对符号   |          |           |
|size    |true          |Integer |返回数据数量 |          |           |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |成交信息     |　         |               |

> 请求参数示例:
```php
{
    "symbol": "BTC/USDT",
    "size" : 30
}
```  

> 接口响应示例:
```php
{
	"code": "200",
	"message": "成功",
	"data": [{
		"symbol": "BTC/USDT",                       // String 交易对符号
		"price": 9096.0,                            // BigDecimal 成交价格
		"amount": 0.1,                              // BigDecimal 成交数量
		"buyTurnover": 0.1,                         // BigDecimal 买方总量
		"sellTurnover": 0.1,                        // BigDecimal 卖方总量
		"direction": "BUY",                         // enum 订单方向 BUY,SELL
		"buyOrderId": "mockBuy1572506652366",       // String 买方订单号
		"sellOrderId": "mockSell1572506652366",     // String 卖方订单号
		"time": 1572506652366                       // Long 撮合时间
	}]
}
```
---
<br>



#### POST /market/exchange-plate 盘口信息

#### 请求参数：

|参数名称    |是否必须    |类型    |描述        |默认值     |取值范围    |
|:---       |:---:      |:---:   |:---        |:---      |---        |
|symbol    |true        |String  |交易对符号   |          |           |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |盘口信息     |　         |               |

> 请求参数示例:
```php
{
    "symbol": "BTC/USDT"
}
```  

> 接口响应示例:
```php

```
---
<br>



### End