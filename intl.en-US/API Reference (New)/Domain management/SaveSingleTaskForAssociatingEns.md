# SaveSingleTaskForAssociatingEns {#concept_593239 .concept}

SaveSingleTaskForAssociatingEns: submits a task for associating an Ethereum wallet address with a domain.

## Description {#section_ev5_eta_oey .section}

You can call this operation to submit a task for associating an Ethereum wallet address with a domain. You can call the [QueryTaskDetailList](https://www.alibabacloud.com/help/doc-detail/67710.htm) operation to query the task execution result.

## Request parameters {#section_16p_fly_nto .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Address|String|Yes|0x1234567890123456789012345678901234567890|The Ethereum address.|
|DomainName|String|Yes|test.com|The domain name.|
|Action|String|No|SaveSingleTaskForAssociatingEns|The operation that you want to perform. Set the value to SaveSingleTaskForAssociatingEns.|
|Lang|String|No|en|The language of the returned error message. Valid values: zh \(Chinese\) and en \(English\). Default value: en|
|UserClientIp|String|No|127.0.0.1|The user client's IP address.|

## Response parameters {#section_aeo_6b8_o4e .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|The ID of the request.|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|The task number.|

## Error codes {#section_a04_ls4_zct .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_lzw_9cy_lcy .section}

``` {#codeblock_ro2_m1i_9lb}
http(s)://[Endpoint]/? Action=SaveSingleTaskForAssociatingEns
&Address=0x1234567890123456789012345678901234567890
&DomainName=test.luxe
&<Common request parameters>
```

## Sample response {#section_3gi_fkd_ls2 .section}

-   XML format

``` {#codeblock_08e_kjx_sov}
<SaveSingleTaskForAssociatingEnsResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForAssociatingEnsResponse>
```

-   JSON format

``` {#codeblock_643_fru_pp9}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


