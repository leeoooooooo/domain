# SaveSingleTaskForSaveArtExtension {#concept_728131 .concept}

SaveSingleTaskForSaveArtExtension: submits a task for configuring the extension information about an .art domain.

## Description {#section_2zn_io1_y03 .section}

You can call this operation to submit a task for configuring the extension information about an .art domain. You can call the [QueryTaskDetailList](https://www.alibabacloud.com/help/doc-detail/67710.htm) operation to query the task execution results.

## Request parameters {#section_0bf_fj7_nm5 .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|No|SaveSingleTaskForSaveArtExtension|The operation that you want to perform. Set the value to SaveSingleTaskForSaveArtExtension.|
|Subject|String|No|subject|The subject of the art object.|
|Features|String|No|features|The features of the art object.|
|Reference|String|No|reference|The references for the art object.|
|Lang|String|No|en|The language of the returned error message. Valid values: zh \(Chinese\) and en \(English\). Default value: en|
|DomainName|String|Yes|test.art|The domain name.|
|ObjectType|String|No|object type|The category of the art object.|
|MaterialsAndTechniques|String|No|materials and techniques|The materials and technique used to make the art object.|
|Dimensions|String|No|dimensions|The dimensions of the art object.|
|Title|String|No|title|The name of the art object.|
|DateOrPeriod|String|No|date or period|The date when the art object was created.|
|Maker|String|No|maker|The name of the artist or maker who created the art object.|
|InscriptionsAndMarkings|String|No|inscriptions and markings|The inscriptions and marks on the art object.|

## Response parameters {#section_hio_etc_uhg .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AB|The ID of the request.|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e141|The task number.|

## Error codes {#section_b0g_7mg_kql .section}

The operation returns only common errors. For more information about errors common to all operations, see [common errors](https://error-center.alibabacloud.com/status/product/Domain).

## Sample request {#section_del_xd7_rbd .section}

``` {#codeblock_vys_vxb_ix2}
http(s)://[Endpoint]/? Action=SaveSingleTaskForSaveArtExtension
&ObjectType=objtype
&MaterialsAndTechniques=materials
&Dimensions=dimensions
&DomainName=test.art
&Title=title
&DateOrPeriod=2018-10-10
&Maker=someone
&InscriptionsAndMarkings=marking
&Subject=subject
&Features=features
&Reference=reference
&<Common request parameters>
```

## Sample response {#section_7e4_2ea_8td .section}

-   XML format

``` {#codeblock_sxe_y46_xsi}
<SaveSingleTaskForSaveArtExtensionResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-6e2a4116e141</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-B42A33C178AB</RequestId>
</SaveSingleTaskForSaveArtExtensionResponse>
```

-   JSON format

``` {#codeblock_5j6_hlu_mv3}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AB",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e141"
}
```


