# 提交删除DS记录任务 {#concept_593220 .concept}

SaveSingleTaskForDeletingDSRecord：提交删除DS记录任务

## 描述 {#section_r27_f0z_3sr .section}

提交删除DS记录任务。任务执行结果请通过查询任务详情[QueryTaskDetailList](intl.zh-CN/API 参考/域名管理接口/查询任务详情.md#)。

## 请求参数 {#section_oqj_c9k_6ed .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|DomainName|String|是|test.com|域名|
|KeyTag|Integer|是|1|关键标签，用于标 识DNSSEC记录，为小于65536的整数值|
|Action|String|否|SaveSingleTaskForDeletingDSRecord|系统规定参数。取值：SaveSingleTaskForDeletingDSRecord。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|UserClientIp|String|否|127.0.0.1|用户IP|

## 返回参数 {#section_0ka_ik6_kcl .section}

|参数|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|唯一请求识别码|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|任务编号|

## 错误码 {#section_gci_2kt_8qa .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_6zv_iq6_1gi .section}

``` {#codeblock_vja_dwc_82f}
http(s)://[Endpoint]/?Action=SaveSingleTaskForDeletingDSRecord
&DomainName=test.com
&KeyTag=1
&<公共请求参数>
```

## 返回示例 {#section_578_puv_bme .section}

-   XML示例

``` {#codeblock_5w2_xwr_rtw}
<SaveSingleTaskForDeletingDSRecordResponse>
  <TaskNo>612db86b-4d8e-44ab-8d54-8d3fb3c0c582</TaskNo>
  <RequestId>2D347ECF-6D8E-4202-8236-692362D8D004</RequestId>
</SaveSingleTaskForDeletingDSRecordResponse>
```

-   JSON示例

``` {#codeblock_sdz_gf2_9ep}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


