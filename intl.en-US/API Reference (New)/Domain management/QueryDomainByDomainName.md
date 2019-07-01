# QueryDomainByDomainName {#concept_610466 .concept}

QueryDomainByDomainName: queries the basic information about a specific domain.

## Description {#section_7p5_4wx_qj0 .section}

You can call this operation to query the basic information about a specific domain.

## Request parameters {#section_rfz_ula_gqc .section}

For more information about common request parameters, see [Public parameters](reseller.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|---------|----|--------|-----------|
|Action|String|Yes|The operation that you want to perform. Set the value to QueryDomainByDomainName.|
|DomainName|String|Yes|The domain name.|

## Response parameters {#section_m3r_ark_omi .section}

|Parameter|Type|Description|
|---------|----|-----------|
|RequestId|String|The ID of the request.|
|UserId|String|The ID of an Alibaba Cloud user.|
|DomainName|String|The domain name.|
|InstanceId|String|The instance ID of the domain.|
|RegistrationDate|String|The registration date of the domain.|
|ExpirationDate|String|The expiration date of the domain.|
|RegistrantOrganization|String|The registrant of the domain.|
|RegistrantName|String|The contact person of the domain.|
|Email|String|The email address of the registrant.|
|EmailVerificationClientHold|Boolean|Indicates whether the domain is client held.|
|EmailVerificationStatus|Boolean|Indicates whether the email address has been verified. Valid values: -   0: not verified
-   1: verified

 |
|UpdateProhibitionLock|String|The status of the update prohibition lock for the domain. Valid values: -   NONE\_SETTING: not set
-   OPEN: enabled
-   CLOSE: disabled

 |
|TransferProhibitionLock|String|The status of the transfer prohibition lock for the domain. Valid values: -   NONE\_SETTING: not set
-   OPEN: enabled
-   CLOSE: disabled

 |
|DomainNameProxyService|Boolean|Indicates whether privacy protection is enabled for the domain.|
|Premium|Boolean|Indicates whether the domain name is a premium word.|
|DnsList|DnsListType|The DNS server list.|
|RealNameStatus|String|The real-name authentication status of the domain. Valid values: -   NONAUDIT: real-name authentication not performed
-   SUCCEED: real-name authentication succeeded
-   FAILED: real-name authentication failed
-   AUDITING: real-name authentication is being reviewed

 |
|RegistrantInfoStatus|String|The modification status of domain information. Valid values: -   NORMAL: registrant information is not being modified
-   PENDING: registrant information is being modified

 |
|TransferOutStatus|String|The transfer-out status of the domain name. Valid values: -   NORMAL: not being transferred
-   PENDING: being transferred out from www.net.cn

 |
|RegistrantType|String|The type of the registrant. Valid values: -   1: individual
-   2: enterprise

 |

## Error codes {#section_n7f_u32_f96 .section}

|Error code|Error message|HTTP status code|Description|
|----------|-------------|----------------|-----------|
|ParameterIllegal|Parameter illegal.|400|The error message returned because a parameter error has occurred.|
|NetworkIOError|Network IO Error.|400|The error message returned because a network I/O exception has occurred.|

## Sample request {#section_u7l_sl4_urc .section}

``` {#codeblock_838_rtv_o44}
http://domain.aliyuncs.com/?Action=QueryDomainByDomainName
&DomainName=test.com
&<Common request parameters>
```

## Sample response {#section_fyd_2aw_sve .section}

-   XML format

``` {#codeblock_29s_4yp_3ot}
<? xml version='1.0' encoding='UTF-8'? >
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

-   JSON format

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


## Sample error response {#section_ts1_32v_ung .section}

-   XML format

    ``` {#codeblock_syx_hb3_of5}
    <Error>
      <RequestId>44101664-3E70-4F0E-89E5-CCB74BF22147</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>InvalidPageSize</Code>
      <Message>Specified parameter PageSize is not valid. </Message>
      <Recommend><![ CDATA[https://error-center.aliyun.com/status/search?Keyword=InvalidPageSize&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON format

    ``` {#codeblock_k11_9fw_p9c}
    {
        "Code":"InvalidPageSize",
        "HostId":"domain.aliyuncs.com",
        "Message":"Specified parameter PageSize is not valid.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=InvalidPageSize&source=PopGw",
        "RequestId":"4B82FF49-B748-4AF0-9F28-D4F8FCDDF52F"
    }
    ```


