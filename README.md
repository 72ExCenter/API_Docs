
# 欢迎使用 「72EX」 API 文档

**72EX 是一个加密货币综合应用平台。
72EX 和根据 72EX 发行的 App 由 Nemoia Global Ltd. 及 Nemoia Capital 全资拥有和经营**


![72EX](https://www.72ex.io/logo.png "72EX")


[72EX（WWW.72EX.IO）](https://www.72ex.io)是一家注册于塞舌尔的加密货币综合应用平台，由Nemoia Global Ltd全资控股经营，Company Number：215264 72EX的技术团队由新加坡、美国、中国等多个国家的专业人才组成，在美国硅谷和新加坡均设有运营点。除此之外，我们还在美国设立了风投基金Nemoia Capital。

72EX作为全球首个跨界交易所，目的不仅仅是作为一个交易媒介，将重点打造加密货币综合应用平台，涵盖游戏娱乐、应用分发、现货期货交易等业务。

---


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
            <td><a href="./wiki/user-center.md" target="_blank" rel="nofollow">用户钱包信息</a></td>
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
            <td><a href="#" target="_blank" rel="nofollow">添加委托</a></td>
        </tr>    
        <tr>
            <td>2</td>
            <td><code>POST /exange/api/v1/order/history</code></td>
            <td><a href="#" target="_blank" rel="nofollow">历史委托</a></td>
        </tr>   
        <tr>
            <td>3</td>
            <td><code>POST /exange/api/v1/order/current</code></td>
            <td><a href="#" target="_blank" rel="nofollow">当前委托</a></td>
        </tr>   
        <tr>
            <td>4</td>
            <td><code>POST /exange/api/v1/order/cancel/{orderId}</code></td>
            <td><a href="#" target="_blank" rel="nofollow">取消委托</a></td>
        </tr> 
    </tbody>
</table>







### End