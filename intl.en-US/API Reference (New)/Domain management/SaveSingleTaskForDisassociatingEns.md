# SaveSingleTaskForDisassociatingEns {#concept_610533 .concept}

SaveSingleTaskForDisassociatingEns: submits a task for disassociating an Ethereum wallet address from a domain.

## Description {#section_2fm_ksr_8gp .section}

You can call this operation to submit a task for disassociating an Ethereum wallet address from a domain. You can the [QueryTaskDetailList](reseller.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) operation to query the task execution result.

## Request parameters {#section_vsd_c7k_nv0 .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|DomainName|String|Yes|test.luxe|The domain name.|
|Action|String|No|SaveSingleTaskForDisassociatingEns|The operation that you want to perform. Set the value to SaveSingleTaskForDisassociatingEns.|
|Lang|String|No|en|The language of the returned error message.|
|UserClientIp|String|No|127.0.0.1|The user client's IP address.|

## Response parameters {#section_w6l_tvl_l0o .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|The ID of the request.|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|The task number.|

## Error codes {#section_d2m_17w_7a4 .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_5m8_jl9_5tf .section}

``` {#codeblock_mca_sgt_b48}
http(s)://[Endpoint]/? Action=SaveSingleTaskForDisassociatingEns
&DomainName=test.luxe
&<Common request parameters>
```

## Sample response {#section_86b_69g_u8v .section}

-   XML format

``` {#codeblock_gdy_uq7_5pz}
<SaveSingleTaskForDisassociatingEnsResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForDisassociatingEnsResponse>
```

-   JSON format

``` {#codeblock_atc_7g5_6o1}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


