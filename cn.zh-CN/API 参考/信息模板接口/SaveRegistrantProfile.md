# SaveRegistrantProfile {#doc_api_Domain_SaveRegistrantProfile .reference}

调用SaveRegistrantProfile创建或保存域名信息模板。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveRegistrantProfile&type=RPC&version=2018-01-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveRegistrantProfile|系统规定参数。取值：**SaveRegistrantProfile**。

 |
|Address|String|否|zhe jiang sheng hang zhou shi shi li qu shi li zhen shi li da sha 1001 hao|具体的地址。

 |
|City|String|否|hang zhou shi|城市。

 |
|Country|String|否|CN|国家代码，如**CN**，**US**。

 |
|DefaultRegistrantProfile|Boolean|否|false|是否默认模板。

 |
|Email|String|否|82106\*\*\*\*@qq.com|邮箱。

 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。

 |
|PostalCode|String|否|310024|邮政编码。

 |
|Province|String|否|zhe jiang|省份。

 |
|RegistrantName|String|否|li si|联系人名称。

 |
|RegistrantOrganization|String|否|li si|持有者名称。

 |
|RegistrantProfileId|Long|否|3600000|信息模板编号。

 |
|RegistrantProfileType|String|否|common|信息模板类型，该字段无需填写。

 |
|RegistrantType|String|否|1|注册者类型，取值：

 -   **1**：个人；
-   **2**：企业。

 |
|TelArea|String|否|86|电话国家代码。

 |
|TelExt|String|否|1234|电话分机。

 |
|Telephone|String|否|1829756\*\*\*\*|电话。

 |
|UserClientIp|String|否|127.0.0.1|用户IP。

 |
|ZhAddress|String|否|浙江省杭州市示例区示例镇示例大厦1001号|中文地址。

 |
|ZhCity|String|否|杭州市|中文城市。

 |
|ZhProvince|String|否|浙江|中文省份。

 |
|ZhRegistrantName|String|否|李四|中文联系人名称。

 |
|ZhRegistrantOrganization|String|否|李四|中文持有者名称。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RegistrantProfileId|Long|3600000|联系人信息模板ID。

 |
|RequestId|String|D09B153B-294D-42F1-BB61-F1C72136DFD3|唯一请求识别码。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=SaveRegistrantProfile
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<SaveRegistrantProfileResponse>
      <RegistrantProfileId>3600000</RegistrantProfileId>
      <RequestId>D09B153B-294D-42F1-BB61-F1C72136DFD3</RequestId>
</SaveRegistrantProfileResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RegistrantProfileId":"3696573",
	"RequestId":"ECB708B9-A82E-45D7-A230-58231E532A57"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

