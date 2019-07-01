# QueryArtExtension {#concept_728134 .concept}

QueryArtExtension：查询Art扩展信息。

## 描述 {#section_pj8_azs_4yh .section}

查询Art扩展信息。

## 请求参数 {#section_b0g_vbl_hby .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|DomainName|String|是|test.art|域名|
|Action|String|否|QueryArtExtension|系统规定参数。取值：QueryArtExtension。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|UserClientIp|String|否|127.0.0.1|用户IP|

## 返回参数 {#section_cgx_ual_bzt .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|814B2AF0-ED6F-4C13-B41C-8AC0B1023583|唯一请求识别码|
|ObjectType|String|objectType|艺术品分类|
|MaterialsAndTechniques|String|materials|材质与工艺|
|Dimensions|String|dimensions|尺寸|
|Title|String|title|名称|
|DateOrPeriod|String|2019-10-01|创作时间|
|Maker|String|maker|艺术家/创作者|
|InscriptionsAndMarkings|String|markings|题词和标识|
|Subject|String|subject|艺术主题|
|Features|String|features|艺术特征|
|Reference|String|reference|参考|

## 错误码 {#section_j7f_7fb_5hb .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_5vn_j3g_14k .section}

``` {#codeblock_pni_mgs_8ys}
http(s)://[Endpoint]/?Action=QueryArtExtension
&DomainName=test.art
&<公共请求参数>
```

## 返回示例 {#section_lyo_kpt_cq9 .section}

-   XML示例

``` {#codeblock_23y_pw3_u3u}
<QueryArtExtensionResponse>
  <Title>title </Title>
  <Subject>subject</Subject>
  <Reference>reference</Reference>
  <ObjectType>objectType</ObjectType>
  <MaterialsAndTechniques>materials</MaterialsAndTechniques>
  <Maker>maker</Maker>
  <InscriptionsAndMarkings>markings</InscriptionsAndMarkings>
  <Features>features</Features>
  <Dimensions>dimensions</Dimensions>
  <DateOrPeriod>2019-10-01</DateOrPeriod>
  <RequestId>5FF5CB45-F34E-406C-8760-C51972EEC315</RequestId>
</QueryArtExtensionResponse>
```

-   JSON示例

``` {#codeblock_bq4_xrj_2nw}
{
    "DateOrPeriod":"2019-10-01",
    "Dimensions":"dimensions",
    "Features":"features",
    "InscriptionsAndMarkings":"markings",
    "Maker":"maker",
    "MaterialsAndTechniques":"materials",
    "ObjectType":"objectType",
    "Reference":"reference",
    "RequestId":"814B2AF0-ED6F-4C13-B41C-8AC0B1023583",
    "Subject":"subject",
    "Title":"title"
}
```


