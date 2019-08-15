# VerifyEmail {#doc_api_Domain_VerifyEmail .reference}

调用VerifyEmail验证邮箱Token。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=VerifyEmail&type=RPC&version=2018-01-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|VerifyEmail|系统规定参数。取值：**VerifyEmail**。

 |
|Token|String|是|a34d34523a4235b3423e34f|邮箱中收到的Token。

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
|RequestId|String|FD3AD289-83EE-4E32-803A-CF1B3A8EEE64|唯一请求识别码。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=VerifyEmail
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<VerifyEmailResponse>
      <RequestId>FD3AD289-83EE-4E32-803A-CF1B3A8EEE64</RequestId>
</VerifyEmailResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"6ED795BD-192E-4921-B8E5-1BCA6F71186C"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

