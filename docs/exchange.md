## 交易模块


#### API Reference：

|#      |请求方法     |请求类型    |描述     |验签    |
|:---:  |:---       |:---:      |:---:    |:---:   |
|1|[POST /exange/api/v1/order/add](#post-exangeapiv1orderadd-添加委托)|POST|添加委托|是|
|2|[POST /exange/api/v1/order/history](#post-exangeapiv1orderhistory-历史委托)|POST|历史委托|是|
|3|[POST /exange/api/v1/order/current](#post-exangeapiv1ordercurrent-当前委托)|POST|当前委托|是|
|4|[POST /exange/api/v1/order/cancel/{orderId}](#post-exangeapiv1ordercancelorderId-取消委托)|POST|取消委托|是|

---




#### POST /exange/api/v1/order/add 添加委托

#### 请求参数：

|参数名称    |是否必须    |类型           |描述    |默认值     |取值范围    |
|:---:      |:---:       |:---:         |:---:    |:---:      |:---:     |
|direction  |true        |enum          |交易方   |          |BUY, SELL   |
|symbol     |true        |String        |交易对   |          |           |
|price      |true        |BigDecimal    |价格     |          |           |
|amount     |true        |BigDecimal    |数量     |          |           |
|type       |true        |enum          |交易类型 |          |MARKET_PRICE, LIMIT_PRICE|


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---:      |---           |
|data                |true       |array          |用户钱包信息 |　         |               |

> 请求参数示例:
```php
{
    "direction": "BUY",
    "symbol": "BTC/USDT",
    "price": 1,
    "amount": 1,
    "type": "MARKET_PRICE"
}
```  

> 接口响应示例:
```json


```
---




#### POST /exange/api/v1/order/history 历史委托

#### 请求参数：

|参数名称    |是否必须    |类型           |描述    |默认值     |取值范围    |
|:---:      |:---:       |:---:         |:---:    |:---:      |:---:     |
|symbol　    |true       |String   |交易对        |          |           |
|pageNo　    |true       |Integer  |页码          |         |           |
|pageSize　  |true       |Integer  |每页显示数量   |         |           |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |用户钱包信息 |　         |               |

> 请求参数示例:
```php
{
    "symbol": "BTC/USDT",
    "pageNo": 1,
    "pageSize": 10
}
```  

> 接口响应示例:
```json


```
---




#### POST /exange/api/v1/order/current 当前委托

#### 请求参数：

|参数名称    |是否必须    |类型           |描述    |默认值     |取值范围    |
|:---:      |:---:       |:---:         |:---:    |:---:      |:---:     |
|symbol　    |true       |String   |交易对        |          |           |
|pageNo　    |true       |Integer  |页码          |         |           |
|pageSize　  |true       |Integer  |每页显示数量   |         |           |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |用户钱包信息 |　         |               |

> 请求参数示例:
```php
{
    "symbol": "BTC/USDT",
    "pageNo": 1,
    "pageSize": 10
}
```  

> 接口响应示例:
```json


```
---




#### POST /exange/api/v1/order/cancel/{orderId} 取消委托

#### 请求参数：

|参数名称    |是否必须    |类型    |描述     |默认值     |取值范围    |
|:---:       |:---:      |:---:  |:---:    |:---      |:---:       |
|orderId    |true       |String |订单ID，注：路径参数    |          |            |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |用户钱包信息 |　         |               |


> 接口响应示例:
```json


```




