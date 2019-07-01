# QueryArtExtension {#concept_728134 .concept}

QueryArtExtension: queries the extension information about an .art domain.

## Description {#section_pj8_azs_4yh .section}

You can call this operation to query the extension information about an .art domain.

## Request parameters {#section_b0g_vbl_hby .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|DomainName|String|Yes|test.art|The domain name.|
|Action|String|No|QueryArtExtension|The operation that you want to perform. Set the value to QueryArtExtension.|
|Lang|String|No|en|The language of the returned error message. Valid values: zh \(Chinese\) and en \(English\). Default value: en|
|UserClientIp|String|No|127.0.0.1|The user's client IP address.|

## Response parameters {#section_cgx_ual_bzt .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|814B2AF0-ED6F-4C13-B41C-8AC0B1023583|The ID of the request.|
|ObjectType|String|objectType|The category of the art object.|
|MaterialsAndTechniques|String|materials|The materials and technique used to make the art object.|
|Dimensions|String|dimensions|The dimensions of the art object.|
|Title|String|title|The name of the art object.|
|DateOrPeriod|String|2019-10-01|The date when the art object was created.|
|Maker|String|maker|The name of the artist or maker who created the art object.|
|InscriptionsAndMarkings|String|markings|The inscriptions and marks on the art object.|
|Subject|String|subject|The subject of the art object.|
|Features|String|features|The features of the art object.|
|Reference|String|reference|The references for the art object.|

## Error codes {#section_j7f_7fb_5hb .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_5vn_j3g_14k .section}

``` {#codeblock_pni_mgs_8ys}
http(s)://[Endpoint]/? Action=QueryArtExtension
&DomainName=test.art
&<Common request parameters>
```

## Sample response {#section_lyo_kpt_cq9 .section}

-   XML format

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

-   JSON format

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


