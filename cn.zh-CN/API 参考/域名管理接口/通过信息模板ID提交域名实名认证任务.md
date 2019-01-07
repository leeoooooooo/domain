# 通过信息模板ID提交域名实名认证任务 {#concept_q5r_rrr_b2b .concept}

通过信息模板ID提交域名实名认证任务，任务执行结果请通过[QueryTaskDetailList](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询任务详情.md#)接口来查询,域名注册联系人信息和模板联系人信息应该一致。

## 请求参数 {#section_pvj_yrr_b2b .section}

公共请求参数，详见[公共参数](cn.zh-CN/API 参考（推荐版）/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileID。|
|InstanceId|String|可选|域名业务编号。|
|DomainName|String|是|域名。|
|RegistrantProfileId|Long|是|信息模板ID。|
|Lang|String|否|接口返回信息语言，枚举值范围：zh 中文；en 英文。默认为en。|

## 返回参数 {#section_zbg_2sr_b2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 {#section_x3p_3sr_b2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|
|DomainNotExist|The domain name does not exist.|400|域名不存在。|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|该域名存在正在处理中的操作，请稍后再试。|
|ContactNotMatch|Contact is not match.|400|信息模板的所有者名称与域名的所有者名称不一致。|
|DomainAlreadyAuditing|The domain name is on auditing.|400|域名已经在审核中。|
|DomainAlreadyAudited|The domain name is audited.|400|域名已经实名认证通过了。|

## 示例 {#section_eh3_qsr_b2b .section}

**请求示例**

```
http://domain.aliyuncs.com/?Action=SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileID
&DomainName=test.com
&InstanceId=S20178S01HX25321
&RegistrantProfileId=1
&<公共请求参数>
```

**返回示例**

-   XML示例

    ```
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileIDResponse>
        <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
        <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
    </SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileIDResponse>
    ```

-   JSON示例

    ```
    {    
      "Success":true,        
      "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
      "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
    }
    ```


