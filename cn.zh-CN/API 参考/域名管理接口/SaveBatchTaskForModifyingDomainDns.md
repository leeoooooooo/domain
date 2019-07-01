# SaveBatchTaskForModifyingDomainDns {#concept_cwr_dzk_c2b .concept}

SaveBatchTaskForModifyingDomainDns：提交批量修改域名DNS任务，任务执行结果请通过[QueryTaskDetailList](intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)接口来查询。

## 请求参数 {#section_dq5_t3n_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveBatchTaskForModifyingDomainDns。|
|DomainName|[DomainListType](#table_otg_v3n_c2b)|是|域名列表。|
|AliyunDns|Boolean|是|是否修改为阿里云DNS。|
|DomainNameServer|[DnsListType](#table_x31_y3n_c2b)|否|DNS列表\(AliyunDns=false时必填\)。|
|Lang|String|否|接口返回信息的语言，枚举值范围：zh 中文；en 英文。默认为 en。|

|名称|类型|描述|
|:-|:-|:-|
|DomainName|String|域名|

|名称|类型|描述|
|:-|:-|:-|
|dns|String|域名DNS信息|

## 返回参数 {#section_xhw_fjn_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 {#section_nwj_3jn_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_dfv_jjn_c2b .section}

**请求示例**

``` {#codeblock_9jm_e4u_bt5}
http://domain-intl.aliyuncs.com/
?Action=SaveBatchTaskForModifyingDomainDns
&AliyunDns=false
&DomainName.1=test1.com
&DomainName.2=test2.com
&DomainNameServer.1=ns1.test.com
&DomainNameServer.2=ns2.test.com
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_xxd_8tj_dl4}
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveBatchTaskForModifyingDomainDnsResponse>
    <TaskNo>35fb2fb7-d4d6-4478-9408-22cb63696b86</TaskNo>
    <RequestId>6A862A8A-E7AB-4C4E-8946-A74122D9CC4B</RequestId></SaveBatchTaskForModifyingDomainDnsResponse>
    ```

-   JSON示例

    ``` {#codeblock_un0_29i_3ag}
    {
      "requestId": "689C17B3-6AE0-45FB-8E41-4491A02C9999",
      "taskNo": "fce12087-6c9f-4dcd-92df-d3829b7f19bc"
    }
    ```


