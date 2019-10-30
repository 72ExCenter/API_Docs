# 用户模块


#### API Reference：

|#    |请求方法    |请求类型    |描述    |验签    |
|---  |:---:      |:---:      |:----- |-----   |
|1|```POST /uc/api/v1/asset/wallet```|POST|用户钱包信息|是|


<h5 id="wallet">POST /uc/api/v1/asset/wallet    用户钱包信息</h4>

#### 请求参数：

|参数名称    |是否必须    |类型    |描述    |默认值     |取值范围    |
|---        |:---:      |:---:  |:-----  |-----     |-----      |
|　         |           |       |        |          |           |



#### data数据：

|参数名称   |是否必须   |类型     |描述     |默认值     |取值范围   |
|---       |:---:     |:---:   |:-----   |-----     |-----     |
|code     |true       |String  |状态码   |　        |200，500，……|
|message  |true       |String  |状态信息 |　         |SUCCESS，FAILED，……|
|data     |true       |Object  |返回数据 |　         |SUCCESS，FAILED，……|



