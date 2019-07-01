# AcknowledgeTaskResult {#concept_bl2_2qy_b2b .concept}

AcknowledgeTaskResult：确认任务详情结果。任务详情结果确认后，将无法从[PollTaskResult](intl.zh-CN/API 参考/域名管理接口/PollTaskResult.md#)接口中查询到。

## 请求参数 {#section_shn_szk_c2b .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|TaskDetailNo.N|RepeatList|是|2659c29493e94416b297a7691340ccc4|任务详情编号。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_hqz_11l_c2b .section}

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|D6CB3623-4726-4947-AC2B-2C6E673B447C|唯一请求识别码。|
|Result|Integer|1|确认成功数量。|

## 示例 {#section_of5_371_b2b .section}

**请求示例**

``` {#codeblock_x40_r7v_qby}
/?Action=AcknowledgeTaskResult
&TaskDetailNo.1=2659c29493e94416b297a7691340ccc4
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_ln8_20y_3m4}
    <AcknowledgeTaskResultResponse>
      <Result>2</Result>
      <RequestId>25DE4410-3E4D-493E-A5E2-927DB738CCEB</RequestId>
    </AcknowledgeTaskResultResponse>
    ```

-   JSON示例

    ``` {#codeblock_5dr_zmh_qmt}
    {
        "RequestId":"270F04F2-6086-4B54-A86B-A1956F231CEC",
        "Result":2
    }
    ```


**异常返回示例**

-   XML示例

    ``` {#codeblock_000_mz2_bcb}
    <Error>
      <RequestId>3A598F91-51B9-4027-B516-BB2BE3E3352D</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingTaskDetailNo</Code>
      <Message>TaskDetailNo is mandatory for this action.</Message>
      <Recommend><![CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingTaskDetailNo&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_vhi_kzb_ypo}
    {
        "Code":"MissingTaskDetailNo",
        "HostId":"domain.aliyuncs.com",
        "Message":"TaskDetailNo is mandatory for this action.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingTaskDetailNo&source=PopGw",
        "RequestId":"37FCCA3D-5BD7-436D-A1EC-3F2E08F0E71E"
    }
    ```


## 错误码 {#section_nwb_371_b2b .section}

[单击查看本产品错误码](intl.zh-CN/API 参考/附录/错误代码表.md#)。

