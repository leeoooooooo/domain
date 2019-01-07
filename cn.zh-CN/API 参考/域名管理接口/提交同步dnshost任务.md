# 提交同步dnshost任务 {#concept_jtb_nzr_b2b .concept}

SaveSingleTaskForSynchronizingDnsHost：提交同步DNS host任务。用来处理DNS host缺失、不一致等情况。任务执行结果请通过[查询任务详情列表](intl.zh-CN/API 参考（推荐版）/域名管理接口/查询任务详情.md#)接口来查询。

## 请求参数 {#section_pgv_rzr_b2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考（推荐版）/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveSingleTaskForSynchronizingDnsHost。|
|InstanceId|String|是|域名实例编号，可通过查询域名列表接口（[QueryDomainList](intl.zh-CN/API 参考（推荐版）/域名管理接口/查询域名列表.md#)）获得。|
|Lang|String|否|接口返回错误信息语言，枚举值范围：zh 中文，en 英文。默认为en。|

## 返回参数 { .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 { .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|该域名存在正在处理中的操作，请稍后再试。|

## 示例 {#section_vxj_j1s_b2b .section}

**请求示例**

```
http://domain-intl.aliyuncs.com/
?Action=SaveSingleTaskForSynchronizingDnsHost
&InstanceId=ST2017120814571100001303
&<公共请求参数>
```

**返回示例**

-   XML示例

    ```
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveSingleTaskForSynchronizingDnsHostResponse>
    <TaskNo>e9b8e8b4-7334-4548-9cec-c30b6891f292</TaskNo>
    <RequestId>0F1B3547-BE50-4206-8F78-9540FFB85BC1</RequestId>
    </SaveSingleTaskForSynchronizingDnsHostResponse>
    ```

-   JSON示例

    ```
    {
      "requestId": "0F1B3547-BE50-4206-8F78-9540FFB85BC1",
      "taskNo": "e9b8e8b4-7334-4548-9cec-c30b6891f292"
    }
    ```


