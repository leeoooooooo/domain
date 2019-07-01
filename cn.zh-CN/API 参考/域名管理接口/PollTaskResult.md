# PollTaskResult {#concept_gyj_pyk_c2b .concept}

PollTaskResult：获取已经执行完成（包括执行成功和执行失败并超过重试次数）的域名任务详情列表。该接口需要配合[AcknowledgeTaskResult](intl.zh-CN/API 参考/域名管理接口/AcknowledgeTaskResult.md#)确认任务结果。任务结果确认后，对应任务记录将无法从该接口查询到。

## 请求示例 {#section_zw1_rpl_c2b .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|PageNum|Integer|是|1|页码。|
|PageSize|Integer|是|20|分页大小。|
|DomainName|String|否|test.com|域名。|
|InstanceId|String|否|S20181T0WLI85212|业务编号。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|
|TaskNo|String|否|75addb07-28a3-450e-b5ec-test|任务编号。|
|TaskResultStatus|Integer|否|2|任务结果类型，枚举值范围：2 成功；3 失败。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_ovn_cql_c2b .section}

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|E879DC07-38EE-4408-9F33-73B30CD965CD|唯一请求识别码。|
|TotalItemNum|Integer|10|总条数。|
|CurrentPageNum|Integer|1|当前页码。|
|TotalPageNum|Integer|10|总页数。|
|PageSize|Integer|1|分页大小。|
|PrePage|Boolean|false|是否有上一页。|
|NextPage|Boolean|false|是否有下一页。|
|Data|[TaskDetail](#table_v4j_inf_b2b)|[TaskDetail](#table_v4j_inf_b2b)|任务详情列表。|

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|TaskNo|String|b95bc334-f7d8-4f39-8a62-4c4302a243d8|任务编号。|
|TaskDetailNo|String|15fee9d10d514bada66bd08c5723c583|任务详情编号。|
|TaskType|String|CHG\_DNS|任务类型。|
|InstanceId|String|S201817141000000|域名实例编号。|
|DomainName|String|test.com|域名。|
|TaskStatus|String|EXECUTE\_SUCCESS|任务状态。可能值： -   WAITING\_EXECUTE 等待执行
-   EXECUTING 执行中
-   EXECUTE\_SUCCESS 执行成功
-   EXECUTE\_FAILURE 执行失败

 |
|UpdateTime|String|2018-03-26 15:22:18|最近一次任务详情执行时间。|
|CreateTime|String|2018-03-26 15:08:20|任务创建时间。|
|TryCount|Integer|0|任务详情重试次数。|
|ErrorMsg|String|The operation is successful.|任务执行失败消息。|
|TaskStatusCode|Integer|2| 任务状态码。可能值：

 -   0 等待执行
-   1 执行中
-   2 执行成功
-   3 执行失败

 |
|TaskResult|String|test|任务结果。|
|TaskTypeDescription|String|修改DNS|任务类型描述，切换Lang参数，该字段会切换语言。|

## 示例 {#section_of5_377_b2b .section}

**请求示例**

``` {#codeblock_ff6_n3y_r44}
/?Action=PollTaskResult
&PageNum=1
&PageSize=20
&DomainName=test.com
&InstanceId=S20181T0WLI85212
&TaskNo=75addb07-28a3-450e-b5ec-test
&TaskResultStatus=2
&TaskType=1
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_btr_jv8_muj}
    <PollTaskResultResponse>
      <Data>
        <TaskDetail>
          <TryCount>0</TryCount>
          <TaskDetailNo>15fee9d10d514bada66bd08c5723c583</TaskDetailNo>
          <TaskNo>b95bc334-f7d8-4f39-8a62-4c4302a243d8</TaskNo>
          <CreateTime>2018-03-26 15:08:20</CreateTime>
          <InstanceId>S201817141000000</InstanceId>
          <UpdateTime>2018-03-26 15:22:18</UpdateTime>
          <TaskStatus>EXECUTE_SUCCESS</TaskStatus>
          <DomainName>test.com</DomainName>
          <TaskTypeDescription>DNS Modification</TaskTypeDescription>
          <TaskStatusCode>2</TaskStatusCode>
          <ErrorMsg>The operation is successful.</ErrorMsg>
          <TaskType>CHG_DNS</TaskType>
        </TaskDetail>
      </Data>
      <TotalItemNum>10</TotalItemNum>
      <PageSize>1</PageSize>
      <CurrentPageNum>1</CurrentPageNum>
      <RequestId>C2CB6161-7971-4EB6-BC16-92A2BA3816D9</RequestId>
      <TotalPageNum>10</TotalPageNum>
    </PollTaskResultResponse>
    ```

-   JSON示例

    ``` {#codeblock_44w_w31_xoa}
    {
        "CurrentPageNum":1,
        "Data":{
            "TaskDetail":[{
                "CreateTime":"2018-03-26 15:08:20",
                "DomainName":"test.com",
                "ErrorMsg":"The operation is successful.",
                "InstanceId":"S201817141000000",
                "TaskDetailNo":"15fee9d10d514bada66bd08c5723c583",
                "TaskNo":"b95bc334-f7d8-4f39-8a62-4c4302a243d8",
                "TaskStatus":"EXECUTE_SUCCESS",
                "TaskStatusCode":2,
                "TaskType":"CHG_DNS",
                "TaskTypeDescription":"DNS Modification",
                "TryCount":0,
                "UpdateTime":"2018-03-26 15:22:18"
            }]
        },
        "PageSize":1,
        "RequestId":"E879DC07-38EE-4408-9F33-73B30CD965CD",
        "TotalItemNum":10,
        "TotalPageNum":10
    }
    ```


**异常返回示例**

-   XML示例

    ``` {#codeblock_lvh_9f0_0mr}
    <Error>
      <RequestId>3D864CDF-026E-45FE-99C8-B31D0E6A775A</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingPageSize</Code>
      <Message>PageSize is mandatory for this action.</Message>
      <Recommend><![CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingPageSize&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_dt3_rgw_i13}
    {
        "Code":"MissingPageSize",
        "HostId":"domain.aliyuncs.com",
        "Message":"PageSize is mandatory for this action.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingPageSize&source=PopGw",
        "RequestId":"85A308D1-F383-4552-B9E7-8D312218D434"
    }
    ```


## 错误码 {#section_nwb_377_b2b .section}

[单击查看本产品错误码](intl.zh-CN/API 参考/附录/错误代码表.md#)。

