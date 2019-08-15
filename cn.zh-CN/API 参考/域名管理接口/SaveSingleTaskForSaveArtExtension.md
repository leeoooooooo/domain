# SaveSingleTaskForSaveArtExtension {#doc_api_Domain_SaveSingleTaskForSaveArtExtension .reference}

调用SaveSingleTaskForSaveArtExtension提交创建Art扩展信息任务。

提交创建Art扩展信息任务。任务执行结果请通过查询任务详情[QueryTaskDetailList](~~67710~~)。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForSaveArtExtension&type=RPC&version=2018-01-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveSingleTaskForSaveArtExtension|系统规定参数。取值：**SaveSingleTaskForSaveArtExtension**。

 |
|DomainName|String|是|test.art|域名。

 |
|ObjectType|String|否|object type|艺术品分类。

 |
|MaterialsAndTechniques|String|否|materials and techniques|材质与工艺。

 |
|Dimensions|String|否|dimensions|尺寸。

 |
|Title|String|否|title|名称。

 |
|DateOrPeriod|String|否|date or period|创作时间。

 |
|Maker|String|否|maker|艺术家、创作者。

 |
|InscriptionsAndMarkings|String|否|inscriptions and markings|题词和标识。

 |
|Subject|String|否|subject|艺术主题。

 |
|Features|String|否|features|艺术特征。

 |
|Reference|String|否|reference|参考。

 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AB|唯一请求识别码。

 |
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e141|任务编号。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=SaveSingleTaskForSaveArtExtension
&DomainName=test.art
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<SaveSingleTaskForSaveArtExtensionResponse>
    <TaskNo>3cbc5b9f-080d-4b5f-a04b-6e2a4116e141</TaskNo>
    <RequestId>722D0361-93BD-4289-824F-B42A33C178AB</RequestId>
</SaveSingleTaskForSaveArtExtensionResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e141",
	"RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AB"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

