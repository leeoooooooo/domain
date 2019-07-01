# SaveSingleTaskForSynchronizingDSRecord {#concept_593232 .concept}

SaveSingleTaskForSynchronizingDSRecord: submits a task for synchronizing the DS records of a domain.

## Description {#section_c33_v4z_cqv .section}

You can call this operation to submit a task for synchronizing the DS records of a domain. You can call the [QueryTaskDetailList](https://help.aliyun.com/document_detail/67710.html) operation to query the task execution result.

## Request parameters {#section_js3_ab4_wvm .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|DomainName|String|Yes|test.com|The domain name.|
|Action|String|No|SaveSingleTaskForSynchronizingDSRecord|The operation that you want to perform. Set the value to SaveSingleTaskForSynchronizingDSRecord.|
|Lang|String|No|en|The language of the returned error message. Valid values: zh \(Chinese\) and en \(English\). Default value: en|
|UserClientIp|String|No|127.0.0.1|The user client's IP address.|

## Response parameters {#section_d69_eg1_x8i .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|The ID of the request.|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|The task number.|

## Error codes {#section_n8k_1y0_5da .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_qqn_yvc_kzc .section}

``` {#codeblock_iwc_l2w_4mq}
http(s)://[Endpoint]/? Action=SaveSingleTaskForSynchronizingDSRecord
&DomainName=test.com
&<Common request parameters>
```

## Sample response {#section_llf_g3e_i5p .section}

-   XML format

``` {#codeblock_jmx_6jm_soo}
<SaveSingleTaskForSynchronizingDSRecordResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForSynchronizingDSRecordResponse>
```

-   JSON format

``` {#codeblock_c2x_3if_mon}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


