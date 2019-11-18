## Market information module


#### API Reference：

|#      |Request method    |Request type   |Description    |Signature verification   |
|:---:  |:---:       |:---:      |:---:    |:---:   |
|1|[POST /market/latest-trade](#post-marketlatest-trade-real-time-trade-data)|POST|Real-time trade data|Yes|
|2|[POST /market/exchange-plate](#post-marketexchange-plate-order-book-information)|POST|Order book information|Yes|

---
<br>



#### POST /market/latest-trade Real-time trade data

#### Request data:

|Parameter name   |Required or not   |Type   |Description       |default    |Range of values   |
|:---       |:---:      |:---:   |:---        |:---      |---        |
|symbol    |true        |String  |Trading pairs symbol   |          |           |
|size    |true          |Integer |Return data quantity |          |           |


#### data Response data:

|Parameter name            |Required or not   |Type          |Description       |default    |Range of values      |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |Trade information     |　         |               |

> Request parameter example:
```php
{
    "symbol": "BTC/USDT",
    "size" : 30
}
```  

> Interface response example:
```php
{
	"code": "200",
	"message": "Success",
	"data": [{
		"symbol": "BTC/USDT",                       // String Trading pairs symbol	
		"price": 9096.0,                            // BigDecimal trade price
		"amount": 0.1,                              // BigDecimal trade volume
		"buyTurnover": 0.1,                         // BigDecimal The total of buyer
		"sellTurnover": 0.1,                        // BigDecimal The total of seller
		"direction": "BUY",                         // enum Order direction BUY,SELL
		"buyOrderId": "mockBuy1572506652366",       // String Buyer order number
		"sellOrderId": "mockSell1572506652366",     // String Seller order number
		"time": 1572506652366                       // Long Deal time
	}]
}
```
---
<br>



#### POST /market/exchange-plate Order book information

#### Request data:

|Parameter name   |Required or not   |Type   |Description       |default    |Range of values   |
|:---       |:---:      |:---:   |:---        |:---      |---        |
|symbol    |true        |String  |Trading pairs symbol	   |          |           |


#### data Response data:

|Parameter name            |Required or not   |Type          |Description       |default    |Range of values      |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |Order book information     |　         |               |

> Request parameter example:
```php
{
    "symbol": "BTC/USDT"
}
```  

> Interface response example:
```php
{
	"code": "200",
	"message": "Success",
	"data": {
		"ask": {                            // Seller
			"minAmount": 0.1,               // BigDecimal Minimum quantity
			"highestPrice": 9500.0,         // BigDecimal Highest price
			"symbol": "BTC/USDT",           // String  Trading pairs symbol		
			"lowestPrice": 9500.0,          // BigDecimal Lowest price
			"maxAmount": 0.1,               // BigDecimal Maximum quantity
			"items": [{                     // Order list information
				"price": 9500.0,            // Resting order price
				"amount": 0.1               // Resting order quantity
			}],
			"direction": "SELL"             // enum Order direction BUY,SELL
		},
		"bid": {                            // Buyer
			"minAmount": 0.01,
			"highestPrice": 8000.0,
			"symbol": "BTC/USDT",
			"lowestPrice": 8000.0,
			"maxAmount": 0.01,
			"items": [{
				"price": 8000.0,
				"amount": 0.01
			}],
			"direction": "BUY"
		}
	}
}
```
---
<br>



### End