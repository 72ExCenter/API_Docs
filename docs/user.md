## 用户模块


#### API Reference：

|#      |请求方法    |请求类型    |描述    |验签    |
|:---:  |:---       |:---:      |:---    |:---:  |
|1|```POST /uc/api/v1/asset/wallet```|POST|[用户钱包信息](#post-/uc/api/v1/asset/wallet-用户钱包信息)|是|



 





#### POST /uc/api/v1/asset/wallet    用户钱包信息

#### 请求参数：


|参数名称    |是否必须    |类型    |描述    |默认值     |取值范围    |
|:---       |:---:      |:---:  |:---    |:---      |---        |
|　         |           |       |        |          |           |



#### data响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |用户钱包信息 |　         |               |



> 接口响应示例:
```json
{
	"code": "200",
	"message": "SUCCESS",
	"data": [
		{
			"id": 70760,      
			"memberId": 1,
			"coin": {
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
            "coinId": "XXEX",
            "coinName": null,
            "balance": 0,
            "frozenBalance": 0,
            "toReleased": 0,
            "address": "",
            "isLock": 0,
            "canInnerTransfer": false,
            "innerTransferFee": 0.2
        }
    ]
}
```
    