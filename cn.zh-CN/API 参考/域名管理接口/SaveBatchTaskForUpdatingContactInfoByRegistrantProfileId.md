# SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId {#concept_ytw_gzk_c2b .concept}

提交批量域名信息修改任务，任务执行结果请通过[QueryTaskDetailList](cn.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)接口来查询。

## 请求参数 {#section_jy3_wnn_c2b .section}

公共请求参数，详见[公共参数](cn.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId。|
|DomainName|[DomainListType](#table_prl_b4n_c2b)|是|域名列表。|
|RegistrantProfileId|Long|是|信息模板编号。|
|ContactType|String|是|联系人类型，枚举值范围：registrant；admin；billing；tech。|
|TransferOutProhibited|Boolean|可选|是否添加禁止转出限制，此参数只对ContactType=registrant情况下起作用，表示持有者修改后是否限制域名60天转出。默认为false，不限制转出。|
|Lang|String|否|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|

|名称|类型|描述|
|:-|:-|:-|
|DomainName|String|域名|

## 返回参数 {#section_dqs_d4n_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 {#section_ukb_34n_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|
|DomainNotExist|The domain name does not exist.|400|域名不存在。|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|该域名存在正在处理中的操作，请稍后再试。|

## 示例 {#section_tg4_m4n_c2b .section}

**请求示例**

``` {#codeblock_7r4_fnu_03m}
http://domain.aliyuncs.com/?Action=SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId
&RegistrantProfileId=1
&DomainName.1=alibabacloud.com
&DomainName.2=aliyun.com
&ContactType=registrant
&TransferOutProhibited=true
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_cyg_kgq_757}
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveBatchTaskForUpdatingContactInfoByRegistrantProfileIdResponse>
        <TaskNo>880f1579-be51-4dd3-a69d-test</TaskNo>
        <RequestId>EDC28FEC-6BE0-4583-95BC-test</RequestId>
    </SaveBatchTaskForUpdatingContactInfoByRegistrantProfileIdResponse>
    ```

-   JSON示例

    ``` {#codeblock_kuk_w4b_ule}
    {
      "requestId": "464AF466-CA8E-43A8-B61D-test",
      "taskNo": "65de2165-ca09-491f-9fe0-test"
    }
    ```


