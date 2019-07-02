# SaveSingleTaskForDeletingDSRecord {#concept_593220 .concept}

SaveSingleTaskForDeletingDSRecord: submits a task for deleting a DS record.

## Description {#section_r27_f0z_3sr .section}

You can call this operation to submit a task for deleting a DS record. You can call the [QueryTaskDetailList](https://www.alibabacloud.com/help/doc-detail/67710.htm) operation to query the task execution result.

## Request parameters {#section_oqj_c9k_6ed .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|DomainName|String|Yes|test.com|The domain name.|
|KeyTag|Integer|Yes|1|The key tag that is used to mark a DNSSEC record. Valid values: 0 to 65535.|
|Action|String|No|SaveSingleTaskForDeletingDSRecord|The operation that you want to perform. Set the value to SaveSingleTaskForDeletingDSRecord.|
|Lang|String|No|en|The language of the returned error message. Valid values: zh \(Chinese\) and en \(English\). Default value: en|
|UserClientIp|String|No|127.0.0.1|The user client's IP address.|

## Response parameters {#section_0ka_ik6_kcl .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|The ID of the request.|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|The task number.|

## Error codes {#section_gci_2kt_8qa .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_6zv_iq6_1gi .section}

``` {#codeblock_vja_dwc_82f}
http(s)://[Endpoint]/? Action=SaveSingleTaskForDeletingDSRecord
&DomainName=test.com
&KeyTag=1
&<Common request parameters>
```

## Sample response {#section_578_puv_bme .section}

-   XML format

``` {#codeblock_5w2_xwr_rtw}
<SaveSingleTaskForDeletingDSRecordResponse>
  <TaskNo>612db86b-4d8e-44ab-8d54-8d3fb3c0c582</TaskNo>
  <RequestId>2D347ECF-6D8E-4202-8236-692362D8D004</RequestId>
</SaveSingleTaskForDeletingDSRecordResponse>
```

-   JSON format

``` {#codeblock_sdz_gf2_9ep}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


