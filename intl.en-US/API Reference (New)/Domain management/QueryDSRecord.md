# QueryDSRecord {#concept_610196 .concept}

QueryDSRecord: queries the DS records of a domain.

## Description {#section_vdn_iqo_p5c .section}

You can call the QueryDSRecord operation to query the DS records of a domain.

## Request parameters {#section_mk0_vxk_0cl .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|DomainName|String|Yes|test.com|The domain name.|
|Action|String|No|QueryDSRecord|The operation that you want to perform. Set the value to QueryDSRecord.|
|Lang|String|No|en|The language of the returned error message. Valid values: zh \(Chinese\) and en \(English\). Default value: en|
|UserClientIp|String|No|127.0.0.1|The user client's IP address.|

## Response parameters {#section_vrl_2nt_46u .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|814B2AF0-ED6F-4C13-B41C-8AC0B1023583|The ID of the request.|
|DSRecordList|The DS record list.|
|└KeyTag|Integer|1|The key tag that is used to mark a DNSSEC record. Valid values: 0 to 65535.|
|└Algorithm|Integer|1|The number of the used DNSSEC algorithm. For more information, see [Domain Name System Security \(DNSSEC\) Algorithm Numbers](https://www.iana.org/assignments/dns-sec-alg-numbers/dns-sec-alg-numbers.xhtml). Valid values: -   1: RSA/MD5
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
-   15: Ed25519
-   16: Ed448
-   252: reserved for indirect keys
-   253: private algorithm
-   254: private algorithm OID

 |
|└DigestType|Integer|2|The type of the digest algorithm. For more information, see [Delegation Signer \(DS\) Resource Record \(RR\) Type Digest Algorithms](https://www.iana.org/assignments/ds-rr-types/ds-rr-types.xhtml). Valid values: -   1: SHA-1
-   2: SHA-256
-   3: GOST R 34.11-94
-   4: SHA-384

 |
|└Digest|String|f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598|The digest value.|

## Error codes {#section_45f_qsr_hpg .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_nmq_3nh_pgr .section}

``` {#codeblock_r97_1o2_n3m}
http(s)://[Endpoint]/? Action=QueryDSRecord
&DomainName=test.com
&<Common request parameters>
```

## Sample response {#section_0zm_e17_26c .section}

-   XML format

``` {#codeblock_xd5_287_wip}
<QueryDSRecordResponse>
  <DSRecordList>
    <DSRecord>
      <Digest>f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598</Digest>
      <DigestType>2</DigestType>
      <Algorithm>2</Algorithm>
      <KeyTag>11</KeyTag>
    </DSRecord>
    <DSRecord>
      <Digest>a55f53655743cf37f8dd69256f9f8780fd72eef30551fe24e747956221d42095</Digest>
      <DigestType>2</DigestType>
      <Algorithm>2</Algorithm>
      <KeyTag>1</KeyTag>
    </DSRecord>
  </DSRecordList>
  <RequestId>5FF5CB45-F34E-406C-8760-C51972EEC315</RequestId>
</QueryDSRecordResponse>
```

-   JSON format

``` {#codeblock_6d8_4xc_lp1}
{
    "DSRecordList":[
        {
            "Algorithm":2,
            "Digest":"f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598",
            "DigestType":2,
            "KeyTag":11
        },
        {
            "Algorithm":2,
            "Digest":"a55f53655743cf37f8dd69256f9f8780fd72eef30551fe24e747956221d42095",
            "DigestType":2,
            "KeyTag":1
        }
    ],
    "RequestId":"814B2AF0-ED6F-4C13-B41C-8AC0B1023583"
}
```


