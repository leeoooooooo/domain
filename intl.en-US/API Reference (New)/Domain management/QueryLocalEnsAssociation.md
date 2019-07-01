# QueryLocalEnsAssociation {#concept_610542 .concept}

QueryLocalEnsAssociation: queries the Ethereum wallet addresses associated with domains recorded in Alibaba Cloud.

## Description {#section_wlp_yks_46p .section}

You can call this operation to query the associated Ethereum addresses recorded in Alibaba Cloud.

## Request parameters {#section_gmq_j56_6jf .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|DomainName|String|Yes|test.luxe|The domain name.|
|Action|String|No|QueryLocalEnsAssociation|The operation that you want to perform. Set the value to QueryLocalEnsAssociation.|
|Lang|String|No|en|The language of the returned error message. Valid values: zh \(Chinese\) and en \(English\). Default value: en|
|UserClientIp|String|No|127.0.0.1|The user client's IP address.|

## Response parameters {#section_gm4_vvn_k36 .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|0x1234567890123456789012345678901234567890|The ID of the request.|
|Address|String|3ECD5439-39A2-477D-9A19-64FCA1F77EEB|The associated Ethereum addresses recorded in the Alibaba Cloud system.|

## Error codes {#section_r76_lou_6sr .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_bvk_by6_3kz .section}

``` {#codeblock_fjk_slt_ai8}
http(s)://[Endpoint]/? Action=QueryLocalEnsAssociation
&DomainName=test.luxe
&<Common request parameters>
```

## Sample response {#section_qxh_uqk_k90 .section}

-   XML format

``` {#codeblock_57p_8gy_a4i}
<QueryLocalEnsAssociationResponse>
  <Address>0x1234567890123456789012345678901234567890</Address>
  <RequestId>D60028B6-4ED1-486C-BA6E-E0B0A8284BE4</RequestId>
</QueryLocalEnsAssociationResponse>
```

-   JSON format

``` {#codeblock_7rd_y0r_hwp}
{
    "Address":"0x1234567890123456789012345678901234567890",
    "RequestId":"3ECD5439-39A2-477D-9A19-64FCA1F77EEB"
}
```


