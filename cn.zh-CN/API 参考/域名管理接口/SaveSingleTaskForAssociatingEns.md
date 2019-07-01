# SaveSingleTaskForAssociatingEns {#concept_593239 .concept}

SaveSingleTaskForAssociatingEns：提交绑定Ens地址任务。

## 描述 {#section_ev5_eta_oey .section}

提交绑定Ens地址任务。任务执行结果请通过查询任务详情[QueryTaskDetailList](intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)。

## 请求参数 {#section_16p_fly_nto .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|Address|String|是|0x1234567890123456789012345678901234567890|ens地址|
|DomainName|String|是|test.com|域名|
|Action|String|否|SaveSingleTaskForAssociatingEns|系统规定参数。取值：SaveSingleTaskForAssociatingEns。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|
|UserClientIp|String|否|127.0.0.1|用户IP|

## 返回参数 {#section_aeo_6b8_o4e .section}

|参数|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|唯一请求识别码|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|任务编号|

## 错误码 {#section_a04_ls4_zct .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_lzw_9cy_lcy .section}

``` {#codeblock_ro2_m1i_9lb}
http(s)://[Endpoint]/?Action=SaveSingleTaskForAssociatingEns
&Address=0x1234567890123456789012345678901234567890
&DomainName=test.luxe
&<公共请求参数>
```

## 返回示例 {#section_3gi_fkd_ls2 .section}

-   XML示例

``` {#codeblock_08e_kjx_sov}
<SaveSingleTaskForAssociatingEnsResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForAssociatingEnsResponse>
```

-   JSON示例

``` {#codeblock_643_fru_pp9}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


