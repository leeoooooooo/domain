# 提交创建DS记录任务 {#concept_593215 .concept}

SaveSingleTaskForAddingDSRecord：提交创建DS记录任务。

## 描述 {#section_9bb_kcu_x9e .section}

提交创建DS记录任务。任务执行结果请通过查询任务详情[QueryTaskDetailList](intl.zh-CN/API 参考/域名管理接口/查询任务详情.md#)。

## 请求参数 {#section_eek_rtc_c45 .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|Algorithm|Integer|是|1|加密算法编号，详见[Domain Name System Security \(DNSSEC\) Algorithm Numbers](https://www.iana.org/assignments/dns-sec-alg-numbers/dns-sec-alg-numbers.xhtml)。枚举范围： -   1 RSA/MD5
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
-   15 Ed2551916 Ed448
-   252 Reserved for Indirect Keys
-   253 private algorithm
-   254 private algorithm OID

 |
|Digest|String|是|f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598|摘要值|
|DigestType|Integer|是|2|摘要算法类型，详见[Delegation Signer \(DS\) Resource Record \(RR\) Type Digest Algorithms](https://www.iana.org/assignments/ds-rr-types/ds-rr-types.xhtml)。枚举值范围： -   1 SHA-1
-   2 SHA-256
-   3 GOST R 34.11-94
-   4 SHA-384

 |
|Digest|String|是|f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598|摘要值|
|DomainName|String|是|test.com|域名|
|KeyTag|Integer|是|1|关键标签，用于标识DNSSEC记录，为小于65536的整数值|
|Action|String|否|SaveSingleTaskForAddingDSRecord|系统规定参数。取值：SaveSingleTaskForAddingDSRecord。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围： -   zh 中文
-   en 英文

 默认为en。|
|UserClientIp|String|否|127.0.0.1|用户IP|

## 返回参数 {#section_em9_933_36h .section}

|参数|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|唯一请求识别码|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|任务编号|

## 错误码 {#section_dql_l9g_eu7 .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_vuw_58b_69v .section}

``` {#codeblock_zup_33x_6np}
http(s)://[Endpoint]/?Action=SaveSingleTaskForAddingDSRecord
&Algorithm=1
&Digest=f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598
&DigestType=2
&DomainName=test.com
&KeyTag=1
&<公共请求参数>
```

## 返回示例 {#section_qqj_tdl_q4s .section}

-   XML示例

``` {#codeblock_dco_9bp_ixc}
<SaveSingleTaskForAddingDSRecordResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForAddingDSRecordResponse>
```

-   JSON示例

``` {#codeblock_cr6_0qh_gvd}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


## 返回异常示例 {#section_9tf_j75_9cv .section}

``` {#codeblock_ca9_tu0_eat}
null
```

