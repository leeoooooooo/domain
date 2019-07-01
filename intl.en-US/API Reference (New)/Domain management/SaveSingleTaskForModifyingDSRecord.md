# SaveSingleTaskForModifyingDSRecord {#concept_593120 .concept}

SaveSingleTaskForModifyingDSRecord: submits a task for modifying a DS record.

## Description {#section_442_uh6_iiv .section}

You can call this operation to submit a task for modifying a DS record. You can the [QueryTaskDetailList](reseller.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) operation to query the task execution result.

## Request parameters {#section_coa_n0p_zxx .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Algorithm|Integer|Yes|1|The number of the used DNSSEC algorithm. For more information, see [Domain Name System Security \(DNSSEC\) Algorithm Numbers](https://www.iana.org/assignments/dns-sec-alg-numbers/dns-sec-alg-numbers.xhtml). Valid values: -   1: RSA/MD5
-   2: Diffie-Hellman
-   3: DSA/SHA-1
-   5: RSA/SHA-1
-   6: DSA-NSEC3-SHA1
-   7: RSASHA1-NSEC3-SHA1
-   8: RSA/SHA-256
-   10: RSA/SHA-512
-   12: GOST R 34.10-2001
-   13: ECDSA Curve P-256 with SHA-256
-   14: ECDSA Curve P-384 with SHA-384
-   15: Ed2551916 Ed448
-   252: reserved for indirect keys
-   253: private algorithm
-   254: private algorithm OID

 |
|Digest|String|Yes|f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598|The digest value.|
|DigestType|Integer|Yes|2|The type of the digest algorithm. For more information, see [Delegation Signer \(DS\) Resource Record \(RR\) Type Digest Algorithms](https://www.iana.org/assignments/ds-rr-types/ds-rr-types.xhtml). Valid values: -   1: SHA-1
-   2: SHA-256
-   3: GOST R 34.11-94
-   4: SHA-384

 |
|Digest|String|Yes|f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598|The digest value.|
|DomainName|String|Yes|test.com|The domain name.|
|KeyTag|Integer|Yes|1|The key tag that is used to mark a DNSSEC record. Valid values: 0 to 65535.|
|Action|String|No|SaveSingleTaskForModifyingDSRecord|The operation that you want to perform. Set the value to SaveSingleTaskForModifyingDSRecord.|
|Lang|String|No|en|The language of the returned error message. Valid values: -   zh: Chinese
-   en: English

 Default value: en|
|UserClientIp|String|No|127.0.0.1|The user client's IP address.|

## Response parameters {#section_7rf_l9s_auh .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|The ID of the request.|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|The task number.|

## Error codes {#section_d02_kfn_kcm .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_2iw_wto_3rr .section}

``` {#codeblock_ope_t34_fdb}
http(s)://[Endpoint]/? Action=SaveSingleTaskForModifyingDSRecord 
&Algorithm=1 
&Digest=f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598 
&DigestType=2 
&DomainName=test.com 
&KeyTag=1 
&<Common request parameters>
```

## Sample response {#section_afl_6v8_o4k .section}

-   XML format

``` {#codeblock_x7w_ga2_yxp}
<SaveSingleTaskForModifyingDSRecordResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForModifyingDSRecordResponse>
```

-   JSON format

``` {#codeblock_zd5_04e_4an}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


