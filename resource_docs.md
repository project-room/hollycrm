## 1. 批量分配表单

1. 接口地址: 
    
    `http://ip:port/newmedia_app`

2. 请求方式: `GET`
3. 请求 JSON 字段: 
    
    |字段|字段名称|参数类型|是否必填|后端默认值|说明|
    |:--|:---|:------|:------|:--|:--|
    |`callback`|回调函数名称|String|是| | 回调函数 |
    |`data`|数据|String|是|accountId:账户,formIdList:表单id列表,agentIdList:分配坐席id列表 |  |

4. 返回 JSON 字段: 

    __请求成功时, 返回状态码 `200`__. 返回 JSON, 格式是:

    |字段|字段名称|参数类型|说明|
    |:--|:---|:------|:------|
    |`Response`|响应action|String| 响应的action名称 |
    |`ActionID`|action的id|String| action的id |
    |`Command`|命令|String| command的名称 |
    |`Succeed`|成功状态|String| true为访问成功,false为访问失败 |

5. 请求成功返回内容示例:

    ```json
    jQuery331021725983067260368_1556418099720({"Response":"BatchReassignForm","ActionID":"","Command":"Response","Succeed":true})
    ```
