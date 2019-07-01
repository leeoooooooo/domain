# QueryDSRecord {#concept_610196 .concept}

：查询域名DS记录。

## 描述 {#section_vdn_iqo_p5c .section}

QueryDSRecord：查询域名DS记录。

## 请求参数 {#section_mk0_vxk_0cl .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|DomainName|String|是|test.com|域名|
|Action|String|否|QueryDSRecord|系统规定参数。取值：QueryDSRecord。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|UserClientIp|String|否|127.0.0.1|用户IP|

## 返回参数 {#section_vrl_2nt_46u .section}

|参数|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|814B2AF0-ED6F-4C13-B41C-8AC0B1023583|唯一请求识别码|
|DSRecordList|DS记录列表|
|└KeyTag|Integer|1|关键标签，用于标识DNSSEC记录，为小于65536的整数值|
|└Algorithm|Integer|1|加密算法编号，详见[Domain Name System Security \(DNSSEC\) Algorithm Numbers](https://www.iana.org/assignments/dns-sec-alg-numbers/dns-sec-alg-numbers.xhtml)。枚举范围： -   1 RSA/MD5
-   2 Diffie-Hellman
-   3 DSA/SHA-1
-   5 RSA/SHA-1
-   6 DSA-NSEC3-SHA1
-   7 RSASHA1-NSEC3-SHA1
-   8 RSA/SHA-256
-   10 RSA/SHA-512
-   12 GOST R 34.10-2001
-   13 ECDSA Curve P-256 with SHA-256
-   14 ECDSA Curve P-384 with SHA-384
-   15 Ed25519
-   16 Ed448
-   252 Reserved for Indirect Keys
-   253 private algorithm
-   254 private algorithm OID

 |
|└DigestType|Integer|2|摘要算法类型，详见[Delegation Signer \(DS\) Resource Record \(RR\) Type Digest Algorithms](https://www.iana.org/assignments/ds-rr-types/ds-rr-types.xhtml)。枚举值范围： -   1 SHA-1
-   2 SHA-256
-   3 GOST R 34.11-94
-   4 SHA-384

 |
|└Digest|String|f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598|摘要值|

## 错误码 {#section_45f_qsr_hpg .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_nmq_3nh_pgr .section}

``` {#codeblock_r97_1o2_n3m}
http(s)://[Endpoint]/?Action=QueryDSRecord
&DomainName=test.com
&<公共请求参数>
```

## 返回示例 {#section_0zm_e17_26c .section}

-   XML示例

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

-   JSON示例

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


