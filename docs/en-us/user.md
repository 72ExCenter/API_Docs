## User module


#### API Reference：

|#      |Request method	     |Request type    |Description     |Signature verification    |
|:---:  |:---:       |:---:      |:---:    |:---:   |
|1|[POST /uc/api/v1/asset/wallet](#post-ucapiv1assetwallet-Wallet-information)|POST|Wallet information|yes|

---
<br>



#### POST /uc/api/v1/asset/wallet Wallet information

#### Request parameter：

| Parameter name|Required or not|Type|Description  |Default   |Range of values  |
|:---       |:---:      |:---:  |:---    |:---      |---        |
|　         |           |       |        |          |           |


#### Response data：

| Parameter name         |Required or not|Type       |Description      |Default   |Range of values     |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |User wallet information |　         |               |


> Interface response example:
```php
{
	"code": "200",                                
	"message": "SUCCESS",
	"data": [
		{
			"id": 70760,                          // long ID
			"memberId": 1,                        // long User ID
			"coin": {                             // object Cryptocurrency type
				"name": "EKT",                    
				"nameCn": "EKT",                 
				"unit": "EKT",                    
				"status": 0,                     
				"minTxFee": 1,                    
				"cnyRate": 1,                   
				"maxTxFee": 111,                 
				"usdRate": 1,                    
				"enableRpc": 1,                 
				"sort": 13,                          
				"canWithdraw": 1,               
				"canRecharge": 1,               
				"canTransfer": 1,                 
				"canInnerTransfer": 0,            
				"canAutoWithdraw": 1,           
				"withdrawThreshold": 11,         
				"minWithdrawAmount": 1,         
				"maxWithdrawAmount": 111,        
				"coinId": 1234,                   
				"coinDecimals": 8,                
				"isPlatformCoin": 0,             
				"hasLegal": false,              
				"allBalance": null,               
				"coldWalletAddress": null,        
				"hotAllBalance": null,            
				"minerFee": 0,                    
				"withdrawScale": 4,              
				"icon": "https://www.xxxx.com",  
				"minRechargeAmount": 0.1,         
				"innerTransferFee": 0.2           
            },
            "coinId": "XXEX",                     // String Cryptocurrency ID
            "coinName": null,                     // String Cryptocurrency name
            "balance": 0,                         // BigDecimal Available Balance
            "frozenBalance": 0,                   // BigDecimal Blocked balances
            "toReleased": 0,                      // BigDecimal Total amount to be released
            "address": "",                        // String Deposit address
            "isLock": 0,                          // Enum Whether the wallet is locked or not，0:No，1:Yes
            "canInnerTransfer": false,            // boolean Whether to support intra-exchange transfer
            "innerTransferFee": 0.2               // BigDecimal The handling fee for transfer（%）
        }
    ]
}
```
---
<br>



### END


