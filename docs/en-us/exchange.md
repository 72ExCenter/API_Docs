## Trading module


#### API Reference：

|#      |Request method   |Request Type    |Description     |Signature verification    |
|:---:  |:---       |:---:      |:---:    |:---:   |
|1|[POST /exange/api/v1/order/add](#post-exangeapiv1orderadd-add-entrust)|POST|Add Entrust|Yes|
|2|[POST /exange/api/v1/order/history](#post-exangeapiv1orderhistory-history-entrust)|POST|History Entrust|Yes|
|3|[POST /exange/api/v1/order/current](#post-exangeapiv1ordercurrent-current-entrust)|POST|Current Entrust|Yes|
|4|[POST /exange/api/v1/order/cancel/{orderId}](#post-exangeapiv1ordercancelorderId-cancel-entrust)|POST|Cancel Entrust|Yes|

---
<br>



#### POST /exange/api/v1/order/add add Entrust

#### Request data:

|Parameter name   |Required or not   |Type         |Description   |Default    |Range of values  |
|:---:      |:---:       |:---:         |:---:    |:---:      |:---:     |
|direction  |true        |enum          |trading party   |          |BUY, SELL   |
|symbol     |true        |String        |Trading pairs symbol	   |          |           |
|price      |true        |BigDecimal    |Trading price     |          |           |
|amount     |true        |BigDecimal    |Trading  Amount    |          |           |
|type       |true        |enum          |Trading Type |          |MARKET_PRICE, LIMIT_PRICE|


#### Response data:

|Parameter name            |Required or not   |Type         |Description       |Default    |Range of values     |
|:---:                |:---:      |:---:          |:---:      |:---:      |---           |
|data                |true       |String          |Order Id     |　         |               |

> Request parameter example:
```php
{
    "direction": "BUY",
    "symbol": "BTC/USDT",
    "price": 1,
    "amount": 1,
    "type": "MARKET_PRICE"
}
```  

> Interface response example:
```php
{
    "code": "200",
    "message": "SUCCESS",
    "data": "E157250163057150"        // Order Id
}
```
---
<br>



#### POST /exange/api/v1/order/history History Entrust

#### Request data:

|Parameter name   |Required or not   |Type         |Description   |Default    |Range of values  |
|:---:      |:---:       |:---:         |:---:    |:---:      |:---:     |
|symbol　    |true       |String   |Trading pairs symbol	        |          |           |
|pageNo　    |true       |Integer  |page number          |         |           |
|pageSize　  |true       |Integer  |page size   |         |           |


#### Response data:

|Parameter name            |Required or not   |Type         |Description       |Default    |Range of values     |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |Object          |Order page information|　         |               |

> Request parameter example:
```php
{
    "symbol": "BTC/USDT",
    "pageNo": 1,
    "pageSize": 10
}
```  

> Interface response example:
```php
{
    "code": "200",
    "message": "SUCCESS",
    "data": {
        "content": [
             {
                "orderId": "E157241957376230",              // String Order Id
                "memberId": 2074,                           // Long member ID
                "type": "LIMIT_PRICE",                      // enum order tpye MARKET_PRICE,LIMIT_PRICE
                "amount": 1,                                // BigDecimal Buy or sell volume, buy list at market price
                "symbol": "BTC/USDT",                       // String Trading pairs symbol	
                "tradedAmount": 0.8359,                     // BigDecimal trading volume
                "turnover": 4272.2849,                      // BigDecimal Transaction amount, useful for the market price
                "coinSymbol": "BTC",                        // String Cryptocurrency unit
                "baseSymbol": "USDT",                       // String unit of account
                "status": "TRADING",                        // enum order status TRADING,COMPLETED,CANCELLED,OVERTIMED
                "direction": "BUY",                         // enum order direction BUY,SELL
                "price": 9240.8,                            // BigDecimal price
                "time": 1572419573762,                      // Long deal time
                "completedTime": null,                      // Long 
                "canceledTime": null,                       // Long 
                "useDiscount": "0",                         // String Whether to use discount 0:No 1:Yes
                "detail": [                                 // List order detail
                    {
                        "orderId": "E157241957376230",      
                        "price": 5111,                      
                        "amount": 0.8359,                   
                        "turnover": 4272.2849,              
                        "fee": 0.0008359,                   // BigDecimal service charge
                        "time": 1572419573786,              
                        "symbol": "BTC/USDT"                
                    }
                ],
                "robot": 0,
                "completed": false
            }
        ],
        "totalPages": 0,                                    
        "totalElements": 0,                                 
        "last": true,
        "size": 10,
        "number": 1,                                        // current page
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




#### POST /exange/api/v1/order/current Current Entrust

#### Request data:

|Parameter name   |Required or not   |Type         |Description   |Default    |Range of values  |
|:---:      |:---:       |:---:         |:---:    |:---:      |:---:     |
|symbol　    |true       |String   |Trading pairs symbol	        |          |           |
|pageNo　    |true       |Integer  |page number          |         |           |
|pageSize　  |true       |Integer  |page size   |         |           |


#### Response data:

|Parameter name            |Required or not   |Type         |Description       |Default    |Range of values     |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |Object         |Order page information |　         |               |

> Request parameter example:
```php
{
    "symbol": "BTC/USDT",
    "pageNo": 1,
    "pageSize": 10
}
```  

> Interface response example:
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




#### POST /exange/api/v1/order/cancel/{orderId} Cancel Entrust

#### Request data:

|Parameter name   |Required or not   |Type  |Description    |Default    |Range of values  |
|:---:       |:---:      |:---:  |:---:    |:---      |:---:       |
|orderId    |true       |String |Order ID，tips：path param    |          |            |


#### Response data:

|Parameter name            |Required or not   |Type         |Description       |Default    |Range of values     |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |String          |result data   |　         |               |

> Request URL example:
```php
/exange/api/v1/order/cancel/E157250163057150
```  

> Interface response example:
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
