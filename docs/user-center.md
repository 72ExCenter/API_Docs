# 用户模块


#### API Reference：

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>请求方法</th>
            <th>请求类型</th>
            <th>描述</th>
            <th>验签</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td><code>POST /uc/api/v1/asset/wallet</code></td>
            <td>POST</td>
            <td><a href="#wallet">用户钱包信息</a></td>
            <td>是</td>
        </tr>       
    </tbody>
</table>



<h5 id="wallet">POST /uc/api/v1/asset/wallet    用户钱包信息</h4>

#### 请求参数：
					
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
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>       
    </tbody>
</table>


#### 公共响应数据：
					
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