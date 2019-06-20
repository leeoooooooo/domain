# 提交创建Art扩展信息任务 {#concept_728131 .concept}

SaveSingleTaskForSaveArtExtension：提交创建Art扩展信息任务。

## 描述 {#section_2zn_io1_y03 .section}

提交创建Art扩展信息任务。任务执行结果请通过查询任务详情[QueryTaskDetailList](intl.zh-CN/API 参考/域名管理接口/查询任务详情.md#)。

## 请求参数 {#section_0bf_fj7_nm5 .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|Action|String|否|SaveSingleTaskForSaveArtExtension|系统规定参数。取值：SaveSingleTaskForSaveArtExtension。|
|Subject|String|否|subject|艺术主题|
|Features|String|否|features|艺术特征|
|Reference|String|否|reference|参考|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|DomainName|String|是|test.art|域名|
|ObjectType|String|否|object type|艺术品分类|
|MaterialsAndTechniques|String|否|materials and techniques|材质与工艺|
|Dimensions|String|否|dimensions|尺寸|
|Title|String|否|title|名称|
|DateOrPeriod|String|否|date or period|创作时间|
|Maker|String|否|maker|艺术家／创作者|
|InscriptionsAndMarkings|String|否|inscriptions and markings|题词和标识|

## 返回参数 {#section_hio_etc_uhg .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AB|唯一请求识别码|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e141|任务编号|

## 错误码 {#section_b0g_7mg_kql .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_del_xd7_rbd .section}

``` {#codeblock_vys_vxb_ix2}
http(s)://[Endpoint]/?Action=SaveSingleTaskForSaveArtExtension
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
&<公共请求参数>
```

## 返回示例 {#section_7e4_2ea_8td .section}

-   XML示例

``` {#codeblock_sxe_y46_xsi}
<SaveSingleTaskForSaveArtExtensionResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-6e2a4116e141</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-B42A33C178AB</RequestId>
</SaveSingleTaskForSaveArtExtensionResponse>
```

-   JSON示例

``` {#codeblock_5j6_hlu_mv3}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AB",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e141"
}
```


