# SaveSingleTaskForUpdateProhibitionLock {#concept_dbq_dwr_b2b .concept}

SaveSingleTaskForUpdateProhibitionLock：提交禁止更新锁任务。任务执行结果请通过[查询任务详情列表](intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)接口来查询。

## 请求参数 {#section_ncl_kwr_b2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveSingleTaskForUpdateProhibitionLock。|
|DomainName|String|是|域名。|
|Status|Boolean|是|开启关闭状态，取值：开启 true；关闭 false。|
|Lang|String|否|接口返回信息语言，枚举值范围：zh 中文，en 英文。默认为en。|

## 返回参数 {#section_wqs_pwr_b2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 {#section_rbw_swr_b2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_zxg_rc4_c2b .section}

**请求示例**

``` {#codeblock_nh4_71h_0c3}
http://domain-intl.aliyuncs.com/
?Action=SaveSingleTaskForUpdateProhibitionLock
&DomainName=test1.com
&Status=false
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_tea_5ob_a7g}
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveSingleTaskForUpdateProhibitionLockResponse>
        <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
        <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
    </SaveSingleTaskForUpdateProhibitionLockResponse>
    ```

-   JSON示例

    ``` {#codeblock_9mc_bm2_cwf}
    {    
      "TaskNo": "d3babb0a-c939-4c25-8c65-c47b65f5492a",
      "RequestId": "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
    }
    ```


