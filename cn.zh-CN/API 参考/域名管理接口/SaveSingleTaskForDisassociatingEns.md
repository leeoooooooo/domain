# SaveSingleTaskForDisassociatingEns {#concept_610533 .concept}

SaveSingleTaskForDisassociatingEns：提交解绑Ens地址任务。

## 描述 {#section_2fm_ksr_8gp .section}

交解绑Ens地址任务。任务执行结果请通过查询任务详情[查询任务详情](intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)。

## 请求参数 {#section_vsd_c7k_nv0 .section}

|名称|类型|是否必须|示例值|描述|
|--|--|----|---|--|
|DomainName|String|是|test.luxe|域名|
|Action|String|否|SaveSingleTaskForDisassociatingEns|系统规定参数。取值：SaveSingleTaskForDisassociatingEns。|
|Lang|String|否|en|用户ip|
|UserClientIp|String|否|127.0.0.1|域名|

## 返回参数 {#section_w6l_tvl_l0o .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|唯一请求识别码|
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|任务编号|

## 错误码 {#section_d2m_17w_7a4 .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Domain)

## 请求示例 {#section_5m8_jl9_5tf .section}

``` {#codeblock_mca_sgt_b48}
http(s)://[Endpoint]/?Action=SaveSingleTaskForDisassociatingEns
&DomainName=test.luxe
&<公共请求参数>
```

## 返回示例 {#section_86b_69g_u8v .section}

-   XML示例

``` {#codeblock_gdy_uq7_5pz}
<SaveSingleTaskForDisassociatingEnsResponse>
  <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
  <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForDisassociatingEnsResponse>
```

-   JSON示例

``` {#codeblock_atc_7g5_6o1}
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```


