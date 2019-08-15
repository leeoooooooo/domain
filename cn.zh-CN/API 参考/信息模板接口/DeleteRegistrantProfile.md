# DeleteRegistrantProfile {#doc_api_Domain_DeleteRegistrantProfile .reference}

调用DeleteRegistrantProfile删除指定的域名信息模板。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=DeleteRegistrantProfile&type=RPC&version=2018-01-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteRegistrantProfile|系统规定参数。取值：**DeleteRegistrantProfile**。

 |
|RegistrantProfileId|Long|是|3600000|信息模板编号。

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
|RequestId|String|C50E41A0-09F1-4491-8DB8-AF55BD2D0CC8|唯一请求识别码。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DeleteRegistrantProfile
&RegistrantProfileId=3600000
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteRegistrantProfileResponse>
      <RequestId>C50E41A0-09F1-4491-8DB8-AF55BD2D0CC8</RequestId>
</DeleteRegistrantProfileResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"0B22A572-0A57-4510-B233-4620D5DE33FE"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

