# QueryRegistrantProfiles {#doc_api_Domain_QueryRegistrantProfiles .reference}

调用QueryRegistrantProfiles查询自己账户下的域名信息模板。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryRegistrantProfiles&type=RPC&version=2018-01-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryRegistrantProfiles|系统规定参数。取值：**QueryRegistrantProfiles**。

 |
|DefaultRegistrantProfile|Boolean|否|false|是否默认模板。取值：

 -   **true**：默认模板；
-   **false**：非默认模板。

 |
|Email|String|否|82106\*\*\*\*@qq.com|电子邮箱。

 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。

 |
|PageNum|Integer|否|1|分页的页码。

 |
|PageSize|Integer|否|500|分页的每页记录数。

 |
|RealNameStatus|String|否|SUCCEED|实名认证状态。取值：

 -   **FAILED**：实名认证失败；
-   **SUCCEED**：实名认证成功；
-   **NONAUDIT**：未实名认证；
-   **AUDITING**：审核中。

 |
|RegistrantOrganization|String|否|li si|域名持有者名称。

 |
|RegistrantProfileId|Long|否|1234567|联系人模板ID。

 |
|RegistrantProfileType|String|否|common|信息模板类型，该字段不用填写。

 |
|RegistrantType|String|否|1|域名持有者类型。取值：

 -   **1**：个人；
-   **2**： 企业。

 |
|UserClientIp|String|否|127.0.0.1|用户IP。

 |
|ZhRegistrantOrganization|String|否|李四|中文持有者名称。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageNum|Integer|1|当前页码。

 |
|NextPage|Boolean|true|是否有下一页。

 |
|PageSize|Integer|2|每页的记录数。

 |
|PrePage|Boolean|false|是否有上一页。

 |
|RegistrantProfiles| | |域名信息模板列表。

 |
|Address|String|zhe jiang sheng hang zhou shi shi li qu shi li zhen shi li da sha 1001 hao|具体的地址。

 |
|City|String|hang zhou shi|城市。

 |
|Country|String|CN|国家代码，如**CN**，**US**。

 |
|CreateTime|String|2019-02-18 10:46:47|创建时间。

 |
|DefaultRegistrantProfile|Boolean|false|是否为默认模板。

 |
|Email|String|82106\*\*\*\*@qq.com|电子邮箱。

 |
|EmailVerificationStatus|Integer|1|邮箱验证状态。取值：

 -   **0**：未验证；
-   **1**：已验证。

 |
|PostalCode|String|310024|邮政编码。

 |
|Province|String|zhe jiang|省份。

 |
|RealNameStatus|String|SUCCEED|实名认证状态。取值：

 -   **FAILED**：实名认证失败；
-   **SUCCEED**：实名认证成功；
-   **NONAUDIT**：未实名认证；
-   **AUDITING**：审核中。

 |
|RegistrantName|String|ls|联系人名称。

 |
|RegistrantOrganization|String|pop|持有者名称。

 |
|RegistrantProfileId|Long|1000001|域名信息模板ID。

 |
|RegistrantProfileType|String|common|信息模板类型。

 |
|RegistrantType|String|1|持有者类型。取值：

 -   **1**：个人；
-   **2**：企业。

 |
|TelArea|String|86|电话国家代码。

 |
|TelExt|String|1234|电话分机。

 |
|Telephone|String|1829756\*\*\*\*|电话。

 |
|UpdateTime|String|2019-03-15 15:32:45|更新时间。

 |
|ZhAddress|String|浙江省杭州市示例区示例镇示例大厦1001号|中文地址。

 |
|ZhCity|String|杭州市|中文城市。

 |
|ZhProvince|String|浙江|中文省份。

 |
|ZhRegistrantName|String|李四|中文联系人名称。

 |
|ZhRegistrantOrganization|String|李四|中文持有者名称。

 |
|RequestId|String|94053D79-7455-4F71-BF06-20EB2DEDE6BD|唯一请求识别码。

 |
|TotalItemNum|Integer|9|总记录数。

 |
|TotalPageNum|Integer|1|总页码。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=QueryRegistrantProfiles
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<QueryRegistrantProfilesResponse>
    <TotalItemNum>9</TotalItemNum>
    <PageSize>500</PageSize>
    <CurrentPageNum>1</CurrentPageNum>
    <RequestId>94053D79-7455-4F71-BF06-20EB2DEDE6BD</RequestId>
    <PrePage>false</PrePage>
    <RegistrantProfiles>
        <RegistrantProfile>
            <ZhCity>杭州市</ZhCity>
            <ZhRegistrantOrganization>李四</ZhRegistrantOrganization>
            <Telephone>1829756****</Telephone>
            <ZhProvince>浙江</ZhProvince>
            <DefaultRegistrantProfile>false</DefaultRegistrantProfile>
            <EmailVerificationStatus>1</EmailVerificationStatus>
            <UpdateTime>2019-03-15 15:32:45</UpdateTime>
            <RealNameStatus>SUCCEED</RealNameStatus>
            <Country>CN</Country>
            <Province>zhe jiang</Province>
            <ZhRegistrantName>李四</ZhRegistrantName>
            <City>hang zhou shi</City>
            <TelArea>86</TelArea>
            <RegistrantProfileId>1000001</RegistrantProfileId>
            <PostalCode>310024</PostalCode>
            <RegistrantType>1</RegistrantType>
            <Email>82106****@qq.com</Email>
            <CreateTime>2019-02-18 10:46:47</CreateTime>
            <Address>zhe jiang sheng hang zhou shi shi li qu shi li zhen shi li da sha 1001 hao</Address>
            <RegistrantName>li si</RegistrantName>
            <RegistrantOrganization>li si</RegistrantOrganization>
            <RegistrantProfileType>common</RegistrantProfileType>
            <ZhAddress>浙江省杭州市示例区示例镇示例大厦1001号</ZhAddress>
        </RegistrantProfile>
    </RegistrantProfiles>
    <TotalPageNum>1</TotalPageNum>
    <NextPage>false</NextPage>
</QueryRegistrantProfilesResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"TotalItemNum":9,
	"CurrentPageNum":1,
	"PageSize":500,
	"RequestId":"94053D79-7455-4F71-BF06-20EB2DEDE6BD",
	"PrePage":false,
	"TotalPageNum":1,
	"RegistrantProfiles":{
		"RegistrantProfile":[
			{
				"ZhCity":"杭州市",
				"ZhRegistrantOrganization":"李四",
				"Telephone":"1829756****",
				"ZhProvince":"浙江",
				"DefaultRegistrantProfile":false,
				"EmailVerificationStatus":1,
				"UpdateTime":"2019-03-15 15:32:45",
				"RealNameStatus":"SUCCEED",
				"Country":"CN",
				"Province":"zhe jiang",
				"ZhRegistrantName":"李四",
				"City":"hang zhou shi",
				"TelArea":"86",
				"RegistrantProfileId":1000001,
				"PostalCode":"310024",
				"Email":"82106****@qq.com",
				"RegistrantType":"1",
				"Address":"zhe jiang sheng hang zhou shi shi li qu shi li zhen shi li da sha 1001 hao",
				"CreateTime":"2019-02-18 10:46:47",
				"RegistrantName":"li si",
				"RegistrantOrganization":"li si",
				"RegistrantProfileType":"common",
				"ZhAddress":"浙江省杭州市示例区示例镇示例大厦1001号"
			}
		]
	},
	"NextPage":false
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

