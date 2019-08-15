# QueryDomainByDomainName {#doc_api_Domain_QueryDomainByDomainName .reference}

调用QueryDomainByDomainName按域名查询域名信息。

根据域名查询域名基本信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryDomainByDomainName&type=RPC&version=2018-01-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryDomainByDomainName|系统规定参数。取值：**QueryDomainByDomainName**。

 |
|DomainName|String|是|test.com|域名。

 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。

 |
|UserClientIp|String|否|127.0.0.1|用户IP。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|DnsList| |dns1.hichina.com,dns2.hichina.com|DNS列表。

 |
|DomainName|String|test.com|域名。

 |
|DomainNameProxyService|Boolean|false|是否已开启隐私保护状态。

 |
|DomainNameVerificationStatus|String|SUCCEED|命名审核状态。取值含义：

 -   **NONAUDIT**： 未认证；
-   **SUCCEED**： 成功；
-   **FAILED**： 审核失败；
-   **AUDITING**： 审核中。

 |
|Email|String|test@alibaba-inc.com|域名所有者邮箱。

 |
|EmailVerificationClientHold|Boolean|false|是否被clienthold。

 |
|EmailVerificationStatus|Integer|1|邮箱是否已通过验证。取值：

 -   **0**：没有通过验证；
-   **1**：已通过验证。

 |
|ExpirationDate|String|2019-12-07 17:02:13|到期时间。

 |
|ExpirationDateLong|Long|1625111915000|到期时间的时间戳。

 |
|InstanceId|String|S20179H1BBI9test|域名实例编号。

 |
|Premium|Boolean|false|是否是溢价词。

 |
|RealNameStatus|String|NONAUDIT|域名实名认证状态。取值：

 -   **NONAUDIT**：未实名认证；
-   **SUCCEED**：成功；
-   **FAILED**：审核失败；
-   **AUDITING**：审核中。

 |
|RegistrantName|String|Test litm|联系人。

 |
|RegistrantOrganization|String|Test litm|域名所有者。

 |
|RegistrantType|String|1|域名注册联系人类型。取值：

 -   **1**：个人；
-   **2**：企业。

 |
|RegistrantUpdatingStatus|String|NORMAL|域名持有者修改状态，取值：

 -   **PENDING** 域名持有者信息修改中
-   **NORMAL** 正常

 |
|RegistrationDate|String|2017-12-07 17:02:13|注册时间。

 |
|RegistrationDateLong|Long|1584675448000|注册时间的时间戳

 |
|RequestId|String|44101664-3E70-4F0E-89E5-CCB74BF22147|唯一请求识别码。

 |
|TransferOutStatus|String|NORMAL|域名转出状态。取值：

 -   **NORMAL**：正常；
-   **PENDING**：正在转出万网。

 |
|TransferProhibitionLock|String|CLOSE|域名转移锁状态。取值：

 -   **NONE\_SETTING**：未设置；
-   **OPEN**：已开启；
-   **CLOSE**：已关闭。

 |
|UpdateProhibitionLock|String|CLOSE|域名安全锁状态。取值：

 -   **NONE\_SETTING**：未设置；
-   **OPEN**：已开启；
-   **CLOSE**：已关闭。

 |
|UserId|String|121000000test|阿里云用户编号。

 |
|ZhRegistrantName|String|李四|中文联系人。

 |
|ZhRegistrantOrganization|String|李四|中文域名持有者。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=QueryDomainByDomainName
&DomainName=test.com
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<QueryDomainByDomainNameResponse>
	  <ZhRegistrantOrganization>李四</ZhRegistrantOrganization>
	  <UpdateProhibitionLock>CLOSE</UpdateProhibitionLock>
	  <InstanceId>S2019270W5******</InstanceId>
	  <ExpirationDateLong>1584675448000</ExpirationDateLong>
	  <ZhRegistrantName>李四</ZhRegistrantName>
	  <DomainNameProxyService>false</DomainNameProxyService>
	  <ExpirationDate>2020-03-20 11:37:28</ExpirationDate>
	  <RegistrantType>1</RegistrantType>
	  <DomainName>test.com</DomainName>
	  <DnsList>
		    <Dns>dns1.hichina.com</Dns>
		    <Dns>dns2.hichina.com</Dns>
	  </DnsList>
	  <TransferProhibitionLock>CLOSE</TransferProhibitionLock>
	  <RegistrationDateLong>1553053048000</RegistrationDateLong>
	  <EmailVerificationStatus>1</EmailVerificationStatus>
	  <RealNameStatus>SUCCEED</RealNameStatus>
	  <UserId>1406926474******</UserId>
	  <Premium>false</Premium>
	  <Email>test@alibaba-inc.com</Email>
	  <RegistrationDate>2019-03-20 11:37:28</RegistrationDate>
	  <RequestId>F5BE26DC-9287-4F1C-B2EB-4124C4ACC349</RequestId>
	  <EmailVerificationClientHold>false</EmailVerificationClientHold>
	  <RegistrantUpdatingStatus>NORMAL</RegistrantUpdatingStatus>
	  <TransferOutStatus>NORMAL</TransferOutStatus>
	  <DomainNameVerificationStatus>SUCCEED</DomainNameVerificationStatus>
	  <RegistrantName>li si</RegistrantName>
	  <RegistrantOrganization>li si</RegistrantOrganization>
</QueryDomainByDomainNameResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"ZhRegistrantOrganization":"李四",
	"UpdateProhibitionLock":"CLOSE",
	"InstanceId":"S2019270W5******",
	"ExpirationDateLong":1584675448000,
	"ZhRegistrantName":"李四",
	"ExpirationDate":"2020-03-20 11:37:28",
	"DomainNameProxyService":false,
	"RegistrantType":"1",
	"DomainName":"test.com",
	"DnsList":{
		"Dns":[
			"dns1.hichina.com",
			"dns2.hichina.com"
		]
	},
	"TransferProhibitionLock":"CLOSE",
	"RegistrationDateLong":1553053048000,
	"EmailVerificationStatus":1,
	"RealNameStatus":"SUCCEED",
	"UserId":"1406926474******",
	"Premium":false,
	"Email":"test@alibaba-inc.com",
	"RegistrationDate":"2019-03-20 11:37:28",
	"RequestId":"F5BE26DC-9287-4F1C-B2EB-4124C4ACC349",
	"EmailVerificationClientHold":false,
	"RegistrantUpdatingStatus":"NORMAL",
	"TransferOutStatus":"NORMAL",
	"DomainNameVerificationStatus":"SUCCEED",
	"RegistrantName":"li si",
	"RegistrantOrganization":"li si"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

