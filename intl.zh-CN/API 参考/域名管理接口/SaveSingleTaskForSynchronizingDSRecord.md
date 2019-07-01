# SaveSingleTaskForSynchronizingDSRecord {#concept_593232 .concept}

SaveSingleTaskForSynchronizingDSRecord：提交同步DS记录任务。

## 描述 {#section_c33_v4z_cqv .section}

提交同步DS记录任务。任务执行结果请通过查询任务详情[QueryTaskDetailList](intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)。

## 请求参数 {#section_js3_ab4_wvm .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|DomainName|String|是|test.com|域名|
|Action|String|否|SaveSingleTaskForSynchronizingDSRecord|系统规定参数。取值：SaveSingleTaskForSynchronizingDSRecord。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|UserClientIp|String|否|127.0.0.1|用户IP|

## 返回参数 {#section_d69_eg1_x8i .section}

|参数|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|唯一请求识别码|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|任务编号|

## 错误码 {#section_n8k_1y0_5da .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_qqn_yvc_kzc .section}

``` {#codeblock_iwc_l2w_4mq}
http(s)://[Endpoint]/?Action=SaveSingleTaskForSynchronizingDSRecord
&DomainName=test.com
&<公共请求参数>
```

## 返回示例 {#section_llf_g3e_i5p .section}

-   XML示例

``` {#codeblock_jmx_6jm_soo}
<SaveSingleTaskForSynchronizingDSRecordResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForSynchronizingDSRecordResponse>
```

-   JSON示例

``` {#codeblock_c2x_3if_mon}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


