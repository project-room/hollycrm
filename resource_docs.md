## 1. 批量分配表单

1. 接口地址: 
    
    `http://ip:port/newmedia_app`

2. 请求方式: `GET`
3. 请求 JSON 字段: 
    
    |字段|字段名称|参数类型|是否必填|后端默认值|说明|
    |:--|:---|:------|:------|:--|:--|
    |`accountId`|账户|String|是| | 账户id |
    |`accountName`|action名称|String|是| | actionName必须赋值为BatchReassignForm |
    |`formIdList`|表单id列表|String|是| | 表单id |
    |`agentIdList`|坐席id列表|String|是| | 坐席id |
4. 请求成功访问内容示例：
    ```
    http://localhost:8081/newmedia_app?callback=jQuery331021725983067260368_1556418099720&data=%7B%22accountId%22%3A%22N000000008597%22%2C%22originalAgentId%22%3A%2290db9383-9d17-47af-87cc-6dee6e34d1e4%22%2C%22targetAgentId%22%3A%2230627c08-9a99-4961-b1bd-308c1973e6e8%22%2C%22skillGroupId%22%3A%22550acc90-64da-11e9-ade2-f7f9d5b5b068%22%2C%22formId%22%3A%2230b9d970-6733-11e9-a83a-cdbca25e1628%22%2C%22Action%22%3A%22BatchReassignForm%22%2C%22Modual%22%3A%22chatForm%22%7D&_=1556418099723
    ```

5. 返回 JSON 字段: 

    __请求成功时, 返回状态码 `200`__. 返回 JSON, 格式是:

    |字段|字段名称|参数类型|说明|
    |:--|:---|:------|:------|
    |`Response`|响应action|String| 响应的action名称 |
    |`ActionID`|action的id|String| action的id |
    |`Command`|命令|String| command的名称 |
    |`Succeed`|成功状态|String| true为访问成功,false为访问失败 |

6. 请求成功返回内容示例:

    ```json
    jQuery331021725983067260368_1556418099720({"Response":"BatchReassignForm","ActionID":"","Command":"Response","Succeed":true})
    ```
