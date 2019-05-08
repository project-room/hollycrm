## 1. 批量分配表单

1. 接口地址: 
    
    `http://ip:port/newmedia_app`

2. 请求方式: `GET`
3. 请求 JSON 字段: 
    
    |字段|字段名称|参数类型|是否必填|后端默认值|说明|
    |:--|:---|:------|:------|:--|:--|
    |`accountId`|账户|String|是| | 账户id |
    |`data`|传参的内容|String|是| | 传参的内容 |
    |`Action`|action名称|String|是| | Action必须赋值为BatchReassignForm,作为data参数内容 |
    |`Modual`|Modual|String|是| | Modual必须赋值为chatForm,作为data参数内容 |
    |`formIdList`|表单id列表|String|是| | 表单id,作为data参数内容 |
    |`agentIdList`|坐席id列表|String|是| | 坐席id,作为data参数内容 |
4. 请求成功访问内容示例：
    ```
    http://localhost:8081/newmedia_app?callback=jQuery331021725983067260368_1556418099720&data={"accountId":"N000000008597","originalAgentId":"90db9383-9d17-47af-87cc-6dee6e34d1e4","targetAgentId":"30627c08-9a99-4961-b1bd-308c1973e6e8","skillGroupId":"550acc90-64da-11e9-ade2-f7f9d5b5b068","formId":"30b9d970-6733-11e9-a83a-cdbca25e1628","Action":"BatchReassignForm","Modual":"chatForm"}&_=1556418099723
    ```
5. 返回 JSON 字段: 

    __请求成功时, 返回状态码 `200`__. 返回 JSON, 格式是:

    |字段|字段名称|参数类型|说明|
    |:--|:---|:------|:------|
    |`Response`|Response|String| Response名称 |
    |`ActionID`|ActionID|String| action的id |
    |`Command`|Command|String| command的名称 |
    |`Succeed`|成功状态|String| true为访问成功,false为访问失败 |

6. 请求成功返回内容示例:

    ```json
    jQuery331021725983067260368_1556418099720({"Response":"BatchReassignForm","ActionID":"","Command":"Response","Succeed":true})
    ```

## 2. 历史会话发送附件
1. 接口地址: 
    
    `http://ip:port/newmedia_app`
2. 请求方式: `POST`
3. 请求 JSON 字段: 
    
    |字段|字段名称|参数类型|是否必填|后端默认值|说明|
    |:--|:---|:------|:------|:--|:--|
    |`Content`|发送文本内容|String|是|发送文本内容,作为data参数内容 |  |
    |`FromUserName`|发送人名称|String|是| | 发送人名称,作为data参数内容 |
    |`ToUserName`|接收人名称|String|是| | 接收人名称,作为data参数内容 |
    |`SequenceID`|序列ID|String|是| | 序列ID,作为data参数内容|
    |`SessionID`|会话id|String|是| | 会话id,作为data参数内容 |
    |`ChannelId`|渠道ID|String|是| | 渠道ID,作为data参数内容 |
    |`AgentId`|坐席id|String|是| | 坐席id,作为data参数内容 |
    |`AgentName`|坐席名称|String|是| | 坐席名称,作为data参数内容 |
    |`SkillGroupId`|技能组id|String|是| | 技能组id,作为data参数内容 |
    |`CustName`|昵称|String|是| | 昵称,作为data参数内容 |
    |`Address`|坐席id列表|String|是| | 坐席id,作为data参数内容 |
    |`VisitorId`|ip地址|String|是| | ip地址,作为data参数内容 |
    |`newMediaEvent`|新媒体事件|String|是| | 新媒体事件,作为data参数内容 |
    |`MsgId`|消息id|String|是| | 消息id,作为data参数内容 |
    |`Action`|action名称|String|是| | action名称,作为data参数内容 |
    |`Mode`|模式|String|是| | 模式,作为data参数内容,作为data参数内容 |
    |`NewMediaType`|新媒体类型|String|是| | 新媒体类型,作为data参数内容 |
    |`Account`|账户|String|是| | 账户,作为data参数内容 |
    |`MsgType`|消息类型|String|是| | 消息类型,作为data参数内容 |
    |`CreateTime`|创建时间|String|是| | 创建时间,作为data参数内容 |
    |`CusNickName`|访客昵称|String|是| | 访客昵称,作为data参数内容 |
    |`CustomerId`|客户id|String|是| | 客户id,作为data参数内容 |
    |`HistorySearchField`|历史字段|String|是| | 历史字段,作为data参数内容 |
    |`attachmentUrl`|附件url|String|是| | 附件url,作为data参数内容 |

