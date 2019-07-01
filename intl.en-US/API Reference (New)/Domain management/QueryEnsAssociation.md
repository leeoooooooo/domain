# QueryEnsAssociation {#concept_593312 .concept}

QueryEnsAssociation: queries the Ethereum wallet addresses associated with domains in ENS.

## Description {#section_9q0_bl3_5bg .section}

You can call this operation to query the Ethereum wallet addresses associated with domains in ENS.

## Request parameters {#section_25u_dog_8na .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|DomainName|String|Yes|test.luxe|The domain name.|
|Action|String|No|QueryEnsAssociation|The operation that you want to perform. Set the value to QueryEnsAssociation.|
|Lang|String|No|en|The language of the returned error message. Valid values: zh \(Chinese\) and en \(English\). Default value: en|
|UserClientIp|String|No|127.0.0.1|The user client's IP address.|

## Response parameters {#section_3vi_u6d_lot .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|3ECD5439-39A2-477D-9A19-64FCA1F77EEB|The ID of the request.|
|Address|String|0x1234567890123456789012345678901234567890|The wallet address in the ENS system.|

## Error codes {#section_jxv_x41_u5l .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_j23_820_slo .section}

``` {#codeblock_giw_9qj_mk6}
http(s)://[Endpoint]/? Action=QueryEnsAssociation
&DomainName=test.luxe
&<Common request parameters>
```

## Sample response {#section_pdn_0re_2ck .section}

-   XML format

``` {#codeblock_2li_d1h_01g}
<QueryEnsAssociationResponse>
  <Address>0x1234567890123456789012345678901234567890</Address>
  <RequestId>D60028B6-4ED1-486C-BA6E-E0B0A8284BE4</RequestId>
</QueryEnsAssociationResponse>
```

-   JSON format

``` {#codeblock_rcs_adz_yik}
{
    "Address":"0x1234567890123456789012345678901234567890",
    "RequestId":"3ECD5439-39A2-477D-9A19-64FCA1F77EEB"
}
```


