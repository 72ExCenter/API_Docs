## 交易模块


#### API Reference：

|#      |请求方法     |请求类型    |描述     |验签    |
|:---:  |:---       |:---:      |:---:    |:---:   |
|1|[POST /exange/api/v1/order/add](#post-exangeapiv1orderadd-添加委托)|POST|添加委托|是|
|2|[POST /exange/api/v1/order/history](#post-exangeapiv1orderhistory-历史委托)|POST|历史委托|是|
|3|[POST /exange/api/v1/order/current](#post-exangeapiv1ordercurrent-当前委托)|POST|当前委托|是|
|4|[POST /exange/api/v1/order/cancel/{orderId}](#post-exangeapiv1ordercancelorderId-取消委托)|POST|取消委托|是|

---
<br>



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
|data                |true       |String          |订单号     |　         |               |

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
```php
{
    "code": "200",
    "message": "SUCCESS",
    "data": "E157250163057150"        // 订单号
}
```
---
<br>



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
|data                |true       |Object          |订单分页信息|　         |               |

> 请求参数示例:
```php
{
    "symbol": "BTC/USDT",
    "pageNo": 1,
    "pageSize": 10
}
```  

> 接口响应示例:
```php
{
    "code": "200",
    "message": "SUCCESS",
    "data": {
        "content": [
             {
                "orderId": "E157241957376230",              // String 订单号
                "memberId": 2074,                           // Long 用户ID
                "type": "LIMIT_PRICE",                      // enum 挂单类型 MARKET_PRICE,LIMIT_PRICE
                "amount": 1,                                // BigDecimal 买入或卖出量，对于市价买入单表
                "symbol": "BTC/USDT",                       // String 交易对符号
                "tradedAmount": 0.8359,                     // BigDecimal 成交量
                "turnover": 4272.2849,                      // BigDecimal 成交额，对市价买单有用
                "coinSymbol": "BTC",                        // String 币单位
                "baseSymbol": "USDT",                       // String 结算单位
                "status": "TRADING",                        // enum 订单状态 TRADING,COMPLETED,CANCELLED,OVERTIMED
                "direction": "BUY",                         // enum 订单方向 BUY,SELL
                "price": 9240.8,                            // BigDecimal 挂单价格
                "time": 1572419573762,                      // Long 挂单时间
                "completedTime": null,                      // Long 交易完成时间
                "canceledTime": null,                       // Long 取消时间
                "useDiscount": "0",                         // String 是否使用折扣 0 不使用 1使用
                "detail": [                                 // List 订单详情
                    {
                        "orderId": "E157241957376230",      
                        "price": 5111,                      
                        "amount": 0.8359,                   
                        "turnover": 4272.2849,              
                        "fee": 0.0008359,                   // BigDecimal 手续费
                        "time": 1572419573786,              
                        "symbol": "BTC/USDT"                
                    }
                ],
                "robot": 0,
                "completed": false
            }
        ],
        "totalPages": 0,                                    // 总页数
        "totalElements": 0,                                 // 总条数
        "last": true,
        "size": 10,
        "number": 1,                                        // 当前页
        "sort": [
            {
                "direction": "DESC",
                "property": "time",
                "ignoreCase": false,
                "nullHandling": "NATIVE",
                "ascending": false,
                "descending": true
            }
        ],
        "first": false,
        "numberOfElements": 0
    }
}
```
---
<br>




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
|data                |true       |Object         |订单分页信息 |　         |               |

> 请求参数示例:
```php
{
    "symbol": "BTC/USDT",
    "pageNo": 1,
    "pageSize": 10
}
```  

> 接口响应示例:
```php
{
    "code": "200",
    "message": "SUCCESS",
    "data": {
        "content": [
            {
                "orderId": "E157250163057150",
                "memberId": 15559,
                "type": "MARKET_PRICE",
                "amount": 1,
                "symbol": "BTC/USDT",
                "tradedAmount": 0,
                "turnover": 0,
                "coinSymbol": "BTC",
                "baseSymbol": "USDT",
                "status": "TRADING",
                "direction": "BUY",
                "price": 0,
                "time": 1572501630570,
                "completedTime": null,
                "canceledTime": null,
                "useDiscount": "0",
                "detail": [],
                "robot": 0,
                "completed": false
            }
        ],
        "totalElements": 1,
        "totalPages": 1,
        "last": true,
        "size": 10,
        "number": 0,
        "sort": [
            {
                "direction": "DESC",
                "property": "time",
                "ignoreCase": false,
                "nullHandling": "NATIVE",
                "ascending": false,
                "descending": true
            }
        ],
        "first": true,
        "numberOfElements": 1
    }
}
```
---
<br>




#### POST /exange/api/v1/order/cancel/{orderId} 取消委托

#### 请求参数：

|参数名称    |是否必须    |类型    |描述     |默认值     |取值范围    |
|:---:       |:---:      |:---:  |:---:    |:---      |:---:       |
|orderId    |true       |String |订单ID，注：路径参数    |          |            |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |String          |处理结果   |　         |               |

> 请求URL示例:
```php
/exange/api/v1/order/cancel/E157250163057150
```  

> 接口响应示例:
```json
{
    "code": "200",
    "message": "SUCCESS",
    "data": "success"
}
```

---
<br>




### END
