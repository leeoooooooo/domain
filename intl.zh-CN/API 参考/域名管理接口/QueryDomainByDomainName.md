# QueryDomainByDomainName {#concept_610466 .concept}

QueryDomainByDomainName：按域名查询域名信息。

## 描述 {#section_7p5_4wx_qj0 .section}

根据域名查询域名基本信息。

## 请求参数 {#section_rfz_ula_gqc .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|--|--|----|--|
|Action|String|是|操作接口名，系统规定参数，取值：QueryDomainByDomainName|
|DomainName|String|是|域名|

## 返回参数 {#section_m3r_ark_omi .section}

|名称|类型|描述|
|--|--|--|
|RequestId|String|唯一请求识别码|
|UserId|String|阿里云用户编号|
|DomainName|String|域名|
|InstanceId|String|域名实例编号|
|RegistrationDate|String|注册时间|
|ExpirationDate|String|到期时间|
|RegistrantOrganization|String|域名所有者|
|RegistrantName|String|联系人|
|Email|String|域名所有者邮箱|
|EmailVerificationClientHold|Boolean|是否被clienthold|
|EmailVerificationStatus|Boolean|邮箱是否已通过验证，枚举值范围： -   0 没有通过验证
-   1 已通过验证

 |
|UpdateProhibitionLock|String|域名安全锁状态，枚举值范围： -   NONE\_SETTING 未设置
-   OPEN 已开启
-   CLOSE 已关闭

 |
|TransferProhibitionLock|String|域名转移锁状态，枚举值范围： -   NONE\_SETTING 未设置
-   OPEN 已开启
-   CLOSE 已关闭

 |
|DomainNameProxyService|Boolean|是否已开启隐私保护状态|
|Premium|Boolean|是否是溢价词|
|DnsList|DnsListType|DNS列表|
|RealNameStatus|String|域名实名认证状态： -   NONAUDIT 未实名认证
-   SUCCEED 成功
-   FAILED 审核失败
-   AUDITING 审核中

 |
|RegistrantInfoStatus|String|域名信息修改状态： -   NORMAL 正常
-   PENDING 域名持有者信息修改中

 |
|TransferOutStatus|String|域名转出状态： -   NORMAL 正常
-   PENDING 正在转出万网

 |
|RegistrantType|String|域名注册联系人类型，枚举值范围： -   1 个人
-   2 企业

 |

## 错误码 {#section_n7f_u32_f96 .section}

|错误代码|描述|HTTP状态码|语义|
|----|--|-------|--|
|ParameterIllegal|Parameter illegal.|400|参数错误|
|NetworkIOError|Network IO Error.|400|网络IO异常|

## 请求示例 {#section_u7l_sl4_urc .section}

``` {#codeblock_838_rtv_o44}
http://domain.aliyuncs.com/?Action=QueryDomainByDomainName
&DomainName=test.com
&<公共请求参数>
```

## 返回示例 {#section_fyd_2aw_sve .section}

-   XML示例

``` {#codeblock_29s_4yp_3ot}
<?xml version='1.0' encoding='UTF-8'?>
<QueryDomainByDomainNameResponse>
    <RegistrantInfoStatus>NORMAL</RegistrantInfoStatus>
    <TransferProhibitionLock>CLOSE</TransferProhibitionLock>
    <UpdateProhibitionLock>CLOSE</UpdateProhibitionLock>
    <InstanceId>S20179H1BBI9test</InstanceId>
    <EmailVerificationStatus>1</EmailVerificationStatus>
    <RealNameStatus>NONAUDIT</RealNameStatus>
    <UserId>121000000test</UserId>
    <Premium>false</Premium>
    <ExpirationDate>2019-12-07 17:02:13</ExpirationDate>
    <DomainNameProxyService>false</DomainNameProxyService>
    <RegistrantType>1</RegistrantType>
    <Email>test@alibaba-inc.com</Email>
    <RegistrationDate>2017-12-07 17:02:13</RegistrationDate>
    <EmailVerificationClientHold>false</EmailVerificationClientHold>
    <DomainName>test.com</DomainName>
    <TransferOutStatus>NORMAL</TransferOutStatus>
    <RegistrantName>Test litm</RegistrantName>
    <DnsList>
        <Dns>dns1.hichina.com</Dns>
        <Dns>dns2.hichina.com</Dns>
    </DnsList>
    <RegistrantOrganization>Test litm</RegistrantOrganization>
</QueryDomainByDomainNameResponse>
```

-   JSON示例

``` {#codeblock_t5u_np9_m6u}
{
  "dnsList": [
    "dns1.hichina.com",
    "dns2.hichina.com"
  ],
  "domainName": "test.com",
  "domainNameProxyService": false,
  "email": "test@alibaba-inc.com",
  "emailVerificationClientHold": false,
  "emailVerificationStatus": 1,
  "expirationDate": "2019-12-07 17:02:13",
  "instanceId": "S20179H1BBI9test",
  "premium": false,
  "realNameStatus": "NONAUDIT",
  "registrantInfoStatus": "NORMAL",
  "registrantName": "Test litm",
  "registrantOrganization": "Test litm",
  "registrationDate": "2017-12-07 17:02:13",
  "transferOutStatus": "NORMAL",
  "transferProhibitionLock": "CLOSE",
  "updateProhibitionLock": "CLOSE",
  "userId": "121000000test"
}
```


## 异常返回示例 {#section_ts1_32v_ung .section}

-   XML示例

    ``` {#codeblock_syx_hb3_of5}
    <Error>
      <RequestId>44101664-3E70-4F0E-89E5-CCB74BF22147</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>InvalidPageSize</Code>
      <Message>Specified parameter PageSize is not valid.</Message>
      <Recommend><![CDATA[https://error-center.aliyun.com/status/search?Keyword=InvalidPageSize&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_k11_9fw_p9c}
    {
        "Code":"InvalidPageSize",
        "HostId":"domain.aliyuncs.com",
        "Message":"Specified parameter PageSize is not valid.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=InvalidPageSize&source=PopGw",
        "RequestId":"4B82FF49-B748-4AF0-9F28-D4F8FCDDF52F"
    }
    ```


