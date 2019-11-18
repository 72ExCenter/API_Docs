## Public method


#### API Reference：

|#      |Method name                                   |Description            |
|:---:  |:---:                                      |:---:            |
|1      |[Request and subscription description](#request-and-subscription-description)       |Request and subscription description      |
|2      |[API public response data](#api-api-public-response-data)       | API public response data      |
|3      |[Signature verification](#signature-verification)                              |User authentication      |

---
<br>



#### Request and subscription description
					
|name          |web site                        |API                    |
|---           |:---:                      |:---:                  |
|development environment      |http://dev.7coins.net       |http://api.7coins.net |
|production environment      |https://www.72ex.io         |https://api.72ex.io   |

---
<br>




#### API public response data
					
|Parameter name  |Required or not  |Type   |Description     |default    |Range of values             |
|---       |:---:      |:---:   |:-----    |-----      |-----                |
|code      |true       |String  |status code    |　          |200，500，……         |
|message   |true       |String  |status message  |　          |SUCCESS，FAILED，……  |
|data      |true       |Object  |return data  |　          |                    |

---
<br>




#### Signature verification
					
|Parameter name   |Required or not  |Type   |Description              |default    |Range of values             |
|---        |:---:      |:---:   |:-----             |-----      |-----                |
|Timestamp  |true       |String  |Time stamp, 1 minute error   |　          |                    |
|Sign       |true       |String  |Signature               |　          |                    |
|AccessKey  |true       |String  |Contact us to get	        |　          |                   |

> Request parameter example:

```php
// req:Request parameter,json type,it is empty string if empty：""
// secretKey:Private key,contact us to get
String Sign = req + "&" + timeStamp + "&" + secretKey;

{
    "Timestamp": timeStamp,
    "Sign": sign,
    "AccessKey": accessKey
}
```

---
<br>




### END

