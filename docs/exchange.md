## 交易模块


#### API Reference：

|#      |请求方法     |请求类型    |描述     |验签    |
|:---:  |:---       |:---:      |:---:    |:---:   |
|1|[POST /exange/api/v1/order/add](#post-exangeapiv1orderadd-添加委托)|POST|添加委托|是|
|1|[POST /exange/api/v1/order/history](#post-exangeapiv1orderhistory-历史委托)|POST|历史委托|是|
|1|[POST /exange/api/v1/order/current](#post-exangeapiv1ordercurrent-当前委托)|POST|当前委托|是|
|1|[POST /exange/api/v1/order/cancel/{orderId}](#post-exangeapiv1ordercancel{orderId}-取消委托)|POST|取消委托|是|


#### POST /exange/api/v1/order/add 添加委托

#### 请求参数：

|参数名称    |是否必须    |类型    |描述    |默认值     |取值范围    |
|:---       |:---:      |:---:  |:---    |:---      |---        |
|　         |           |       |        |          |           |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |用户钱包信息 |　         |               |


> 接口响应示例:
```json


```




#### POST /exange/api/v1/order/history 历史委托

#### 请求参数：

|参数名称    |是否必须    |类型    |描述    |默认值     |取值范围    |
|:---       |:---:      |:---:  |:---    |:---      |---        |
|　         |           |       |        |          |           |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |用户钱包信息 |　         |               |


> 接口响应示例:
```json


```




#### POST /exange/api/v1/order/current 当前委托

#### 请求参数：

|参数名称    |是否必须    |类型    |描述    |默认值     |取值范围    |
|:---       |:---:      |:---:  |:---    |:---      |---        |
|　         |           |       |        |          |           |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |用户钱包信息 |　         |               |


> 接口响应示例:
```json


```




#### POST /exange/api/v1/order/cancel/{orderId} 取消委托

#### 请求参数：

|参数名称    |是否必须    |类型    |描述    |默认值     |取值范围    |
|:---       |:---:      |:---:  |:---    |:---      |---        |
|　         |           |       |        |          |           |


#### data 响应数据：

|参数名称             |是否必须    |类型           |描述        |默认值     |取值范围       |
|:---:                |:---:      |:---:          |:---:      |:---       |---           |
|data                |true       |array          |用户钱包信息 |　         |               |


> 接口响应示例:
```json


```




