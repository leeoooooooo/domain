# 查询阿里云系统中记录的ens绑定地址 {#concept_610542 .concept}

QueryLocalEnsAssociation：查询阿里云系统中记录的ens绑定地址。

## 描述 {#section_wlp_yks_46p .section}

查询阿里云系统中记录的ens绑定地址。

## 请求参数 {#section_gmq_j56_6jf .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|DomainName|String|是|test.luxe|域名|
|Action|String|否|QueryLocalEnsAssociation|系统规定参数。取值：QueryLocalEnsAssociation。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|UserClientIp|String|否|127.0.0.1|用户ip|

## 返回参数 {#section_gm4_vvn_k36 .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|0x1234567890123456789012345678901234567890|唯一请求识别码|
|Address|String|3ECD5439-39A2-477D-9A19-64FCA1F77EEB|阿里云系统中记录的ens地址|

## 错误码 {#section_r76_lou_6sr .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_bvk_by6_3kz .section}

``` {#codeblock_fjk_slt_ai8}
http(s)://[Endpoint]/?Action=QueryLocalEnsAssociation
&DomainName=test.luxe
&<公共请求参数>
```

## 返回示例 {#section_qxh_uqk_k90 .section}

-   XML示例

``` {#codeblock_57p_8gy_a4i}
<QueryLocalEnsAssociationResponse>
  <Address>0x1234567890123456789012345678901234567890</Address>
  <RequestId>D60028B6-4ED1-486C-BA6E-E0B0A8284BE4</RequestId>
</QueryLocalEnsAssociationResponse>
```

-   JSON示例

``` {#codeblock_7rd_y0r_hwp}
{
    "Address":"0x1234567890123456789012345678901234567890",
    "RequestId":"3ECD5439-39A2-477D-9A19-64FCA1F77EEB"
}
```


