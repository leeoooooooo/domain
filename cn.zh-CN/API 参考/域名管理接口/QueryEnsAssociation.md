# QueryEnsAssociation {#concept_593312 .concept}

QueryEnsAssociation：查询Ens系统中绑定的地址。

## 描述 {#section_9q0_bl3_5bg .section}

查询Ens系统中绑定的钱包地址。

## 请求参数 {#section_25u_dog_8na .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|DomainName|String|是|test.luxe|域名|
|Action|String|否|QueryEnsAssociation|系统规定参数。取值：QueryEnsAssociation。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|UserClientIp|String|否|127.0.0.1|用户IP|

## 返回参数 {#section_3vi_u6d_lot .section}

|参数|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|3ECD5439-39A2-477D-9A19-64FCA1F77EEB|唯一请求识别码|
|Address|String|0x1234567890123456789012345678901234567890|ens系统中的钱包地址|

## 错误码 {#section_jxv_x41_u5l .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_j23_820_slo .section}

``` {#codeblock_giw_9qj_mk6}
http(s)://[Endpoint]/?Action=QueryEnsAssociation
&DomainName=test.luxe
&<公共请求参数>
```

## 返回示例 {#section_pdn_0re_2ck .section}

-   XML示例

``` {#codeblock_2li_d1h_01g}
<QueryEnsAssociationResponse>
  <Address>0x1234567890123456789012345678901234567890</Address>
  <RequestId>D60028B6-4ED1-486C-BA6E-E0B0A8284BE4</RequestId>
</QueryEnsAssociationResponse>
```

-   JSON示例

``` {#codeblock_rcs_adz_yik}
{
    "Address":"0x1234567890123456789012345678901234567890",
    "RequestId":"3ECD5439-39A2-477D-9A19-64FCA1F77EEB"
}
```


