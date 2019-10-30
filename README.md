
# 欢迎使用 「72EX」 API 文档

**72EX 是一个加密货币综合应用平台。
72EX 和根据 72EX 发行的 App 由 Nemoia Global Ltd. 及 Nemoia Capital 全资拥有和经营**


![72EX](https://www.72ex.io/logo.png "72EX")


[72EX（WWW.72EX.IO）](https://www.72ex.io)是一家注册于塞舌尔的加密货币综合应用平台，由Nemoia Global Ltd全资控股经营，Company Number：215264 72EX的技术团队由新加坡、美国、中国等多个国家的专业人才组成，在美国硅谷和新加坡均设有运营点。除此之外，我们还在美国设立了风投基金Nemoia Capital。

72EX作为全球首个跨界交易所，目的不仅仅是作为一个交易媒介，将重点打造加密货币综合应用平台，涵盖游戏娱乐、应用分发、现货期货交易等业务。

---


### 公共响应数据：
					
<table>
    <thead>
        <tr>
            <th>参数名称</th>
            <th>是否必须</th>
            <th>类型</th>
            <th>描述</th>
            <th>默认值</th>
            <th>取值范围</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>code</td>
            <td>true</td>
            <td>String</td>
            <td>状态码</td>
            <td></td>
            <td>200，500，……</td>
        </tr>  
        <tr>
            <td>message</td>
            <td>true</td>
            <td>String</td>
            <td>状态信息</td>
            <td></td>
            <td>SUCCESS，FAILED，……</td>
        </tr>  
        <tr>
            <td>data</td>
            <td>true</td>
            <td>object</td>
            <td>返回数据</td>
            <td></td>
            <td></td>
        </tr>       
    </tbody>
</table>


## 用户模块

#### 接口列表：

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>接口</th>
            <th>说明</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td><code>POST /uc/api/v1/asset/wallet</code></td>
            <td><a href="./docs/user-center.md" target="_blank">用户钱包信息</a></td>
        </tr>       
    </tbody>
</table>
   

---

## 交易模块

#### 接口列表：
   
<table>
    <thead>
        <tr>
            <th>#</th>
            <th>接口</th>
            <th>说明</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td><code>POST /exange/api/v1/order/add</code></td>
            <td><a href="./docs/exchange.md" target="_blank">添加委托</a></td>
        </tr>    
        <tr>
            <td>2</td>
            <td><code>POST /exange/api/v1/order/history</code></td>
            <td><a href="./docs/exchange.md" target="_blank">历史委托</a></td>
        </tr>   
        <tr>
            <td>3</td>
            <td><code>POST /exange/api/v1/order/current</code></td>
            <td><a href="./docs/exchange.md" target="_blank">当前委托</a></td>
        </tr>   
        <tr>
            <td>4</td>
            <td><code>POST /exange/api/v1/order/cancel/{orderId}</code></td>
            <td><a href="./docs/exchange.md" target="_blank">取消委托</a></td>
        </tr> 
    </tbody>
</table>







### End