# QueryTransferInByInstanceId {#concept_b3t_wyk_c2b .concept}

QueryTransferInByInstanceId：根据实例编号查询域名转入信息。

## 请求参数 {#section_ahd_f5m_c2b .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|InstanceId|String|是|S20181T0WLI85212|实例编号。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_ahr_j5m_c2b .section}

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|唯一请求识别码。|
|SubmissionDate|String|2018-03-28 00:41:42|转移请求提交时间。|
|ModificationDate|String|2018-03-28 00:41:42|转入信息更新时间。|
|UserId|String|123456|用户编号。|
|InstanceId|String|S20181T0WLI85212|实例编号。|
|DomainName|String|test.com|域名。|
|Status|Integer|11|详细域名转入状态，枚举值范围： -   10 初始状态
-   11 已发送邮件验证token链接
-   19 token连接已验证成功
-   20 已提交命名审核
-   21 命名审核失败
-   29 命名审核成功
-   31 转移密码错误
-   39 转入提交成功
-   50 客户取消转入
-   51 转入失败
-   52 转入过期
-   59 转入成功

 |
|SimpleTransferInStatus|String|SUCCESS|转移状态，枚举值范围： -   INIT 提交转入
-   AUTHORIZATION 授权转入（邮箱验证）
-   NAME\_VERIFICATION 命名审核
-   PASSWORD\_VERIFICATION转移密码验证
-   PENDING 转入处理中
-   SUCCESS 转入成功
-   FAIL 转入失败

 |
|ResultCode|String|clientCancelled|转移失败时失败原因code，枚举值范围： -   clientCancelled 您取消了此次域名转入
-   clientRejected 域名原注册商拒绝了本次域名转入（或您通过原注册商进行了拒绝操作）
-   serverCancelled 注册局取消转入
-   transferProhibited 域名为禁止转移状态
-   transferExpired 您未在有效期内完成相关转入确认
-   nameVerificationFailed 域名命名审核未通过
-   transferSubmitted 其他用户已经提交域名转入

 |
|ResultDate|String|2018-03-28 00:41:42|转移成功或失败的时间。|
|ResultMsg|String|您取消了此次域名转入|转移失败时失败原因描述。|
|TransferAuthorizationCodeSubmissionDate|String|2018-03-28 00:41:42|转移密码提交成功时间。|
|NeedMailCheck|Boolean|true|是否需要邮件验证。|
|Email|String|test@test.com|域名转入确认邮件发送邮箱。|
|WhoisMailStatus|Boolean|true|是否通过whois抓取到域名持有者邮箱。当域名转入处于授权转入（邮箱验证）并且该字段为false时，表示未通过whois抓取到域名持有者邮箱，需要等待人工处理。|
|ExpirationDate|String|2018-03-28 00:41:42|域名转入过期时间。|
|ProgressBarType|Integer|0|转移过程进度条类型，枚举值范围： -   0 同时需要邮箱验证和命名审核
-   1 需要邮箱验证不需要命名审核
-   2 需要邮箱验证不需要命名审核
-   3 不需要邮箱验证不需要命名审核

 |
|SubmissionDateLong|Long|1514428524669|转移请求提交时间戳。|
|ModificationDateLong|Long|1514428524669|转入信息更新时间戳。|
|ResultDateLong|Long|1514428524669|转移成功或失败的时间戳。|
|ExpirationDateLong|Long|1514428524669|转入过期时间戳。|
|TransferAuthorizationCodeSubmissionDateLong|Long|1514428524669|转移密码提交成功时间戳。|

## 示例 {#section_of5_389_b2b .section}

**请求示例**

``` {#codeblock_wg7_i6m_1bl}
/?Action=QueryTransferInByInstanceId
&InstanceId=S20181T0WLI85212
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_k8v_62j_br0}
    <QueryTransferInByInstanceIdResponse>
      <InstanceId>S20182F0RED000000</InstanceId>
      <WhoisMailStatus>true</WhoisMailStatus>
      <UserId>123456</UserId>
      <ResultDate>2018-03-28 09:54:39</ResultDate>
      <ExpirationDate>2018-04-12 09:51:53</ExpirationDate>
      <NeedMailCheck>true</NeedMailCheck>
      <Status>50</Status>
      <Email/>
      <SimpleTransferInStatus>FAIL</SimpleTransferInStatus>
      <ResultMsg>You have canceled this domain name transfer in.</ResultMsg>
      <RequestId>0D6108ED-7BB3-4898-83D0-44883DE0D3E7</RequestId>
      <ModificationDate>2018-03-28 09:54:39</ModificationDate>
      <ResultCode>clientCancelled</ResultCode>
      <DomainName>test.com</DomainName>
      <ProgressBarType>0</ProgressBarType>
      <SubmissionDate>2018-03-28 09:51:53</SubmissionDate>
    </QueryTransferInByInstanceIdResponse>
    ```

-   JSON示例

    ``` {#codeblock_2ka_30o_ps2}
    {
        "DomainName":"test.com",
        "Email":"",
        "ExpirationDate":"2018-04-12 09:51:53",
        "InstanceId":"S20182F0RED000000",
        "ModificationDate":"2018-03-28 09:54:39",
        "NeedMailCheck":true,
        "ProgressBarType":0,
        "RequestId":"B3E437A1-4947-4E4F-B9E2-9781AB1C8134",
        "ResultCode":"clientCancelled",
        "ResultDate":"2018-03-28 09:54:39",
        "ResultMsg":"You have canceled this domain name transfer in.",
        "SimpleTransferInStatus":"FAIL",
        "Status":50,
        "SubmissionDate":"2018-03-28 09:51:53",
        "UserId":"123456",
        "WhoisMailStatus":true
    }
    ```


**异常返回示例**

-   XML示例

    ``` {#codeblock_7zj_ikb_afz}
    <Error>
      <RequestId>41187FF2-262D-4414-8AD2-7B85D74E1385</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingInstanceId</Code>
      <Message>InstanceId is mandatory for this action.</Message>
      <Recommend><![CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingInstanceId&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_ntz_jtu_x0e}
    {
        "Code":"MissingInstanceId",
        "HostId":"domain.aliyuncs.com",
        "Message":"InstanceId is mandatory for this action.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingInstanceId&source=PopGw",
        "RequestId":"05973664-CD29-4CF5-8060-FAC3E2CE0D87"
    }
    ```


## 错误码 {#section_nwb_389_b2b .section}

[单击查看本产品错误码](intl.zh-CN/API 参考/附录/错误代码表.md#)。

