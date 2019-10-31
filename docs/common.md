## 公共方法


#### API Reference：

|#      |方法名称                                    |描述             |
|:---:  |:---:                                      |:---:            |
|1      |[API 公共响应数据](#api-公共响应数据)       |公共响应数据      |
|2      |[验签](#验签)                              |用户身份验证      |

---
<br><br>




#### API 公共响应数据
					
|参数名称   |是否必须   |类型     |描述      |默认值     |取值范围              |
|---       |:---:      |:---:   |:-----    |-----      |-----                |
|code      |true       |String  |状态码    |　          |200，500，……         |
|message   |true       |String  |状态信息  |　          |SUCCESS，FAILED，……  |
|data      |true       |Object  |返回数据  |　          |                    |

---
<br><br>




#### 验签
					
|参数名称    |是否必须   |类型     |描述               |默认值     |取值范围              |
|---        |:---:      |:---:   |:-----             |-----      |-----                |
|Timestamp  |true       |String  |时间戳，1分钟误差   |　          |                    |
|Sign       |true       |String  |签名               |　          |                    |
|AccessKey  |true       |String  |联系我们获取        |　          |                   |

> 请求参数示例:

```php
// req:请求参数,json类型,如果为空则为空字符串：""
// secretKey:私钥,联系我们获取
String Sign = req + "&" + timeStamp + "&" + secretKey;

{
    "Timestamp": timeStamp,
    "Sign": sign,
    "AccessKey": accessKey
}
```

---
<br><br>




### END

