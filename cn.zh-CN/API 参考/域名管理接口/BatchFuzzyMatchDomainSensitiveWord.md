# BatchFuzzyMatchDomainSensitiveWord {#doc_api_Domain_BatchFuzzyMatchDomainSensitiveWord .reference}

调用BatchFuzzyMatchDomainSensitiveWord根据传入参数批量检查域名是否包含敏感词。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=BatchFuzzyMatchDomainSensitiveWord&type=RPC&version=2018-01-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|BatchFuzzyMatchDomainSensitiveWord|系统规定参数。取值：**BatchFuzzyMatchDomainSensitiveWord**。

 |
|Keyword|String|是|abc.com,cbc.com|关键字，多个以逗号（,）分隔。

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
|RequestId|String|BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1|唯一请求识别码。

 |
|SensitiveWordMatchResultList| | |批量匹配结果列表。

 |
|Exist|Boolean|true|是否包含敏感词。

 |
|Keyword|String|abc.com|传入的关键字。

 |
|MatchedSentiveWords| | |匹配结果详情，当**Exist**为**false**时，匹配结果为空。

 |
|Word|String|ab|批配到的敏感词。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=BatchFuzzyMatchDomainSensitiveWord
&Keyword=abc.com,cbc.com
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<BatchFuzzyMatchDomainSensitiveWord>
    <RequestId>BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1</RequestId>
    <SensitiveWordMatchResultList>
        <SensitiveWordMatchResult>
            <Keyword>abc.com</Keyword>
            <Exist>true</Exist>
            <MatchedSentiveWords>
                <MatchedSensitiveWord>
                    <Word>ab<Word/>
                </MatchedSensitiveWord>
            </MatchedSentiveWords>
        </SensitiveWordMatchResult>
        <SensitiveWordMatchResult>
            <Keyword>cbc.com</Keyword>
            <Exist>false</Exist>
        </SensitiveWordMatchResult>
</SensitiveWordMatchResultList>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"SensitiveWordMatchResultList":{
		"SensitiveWordMatchResult":[
			{
				"Keyword":"abc.com",
				"Exist":false
			},
			{
				"Keyword":"cbc.com",
				"Exist":false
			}
		]
	},
	"RequestId":"CD70DBC3-62F1-41BA-AD9A-D6B28F0A6BFE"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

