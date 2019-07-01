# SaveSingleTaskForCreatingOrderRedeem {#concept_tl1_jsp_b2b .concept}

提交域名赎回任务，任务执行结果请通过[查询任务详情](intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)接口来查询。

## 请求参数 {#section_irp_dwn_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveSingleTaskForCreatingOrderRedeem。|
|DomainName|String|是|域名。|
|CurrentExpirationDate|Long|是|域名当前到期时间，UTC时间1970年1月1日0点距离现在的毫秒数。|
|Lang|String|否|接口返回信息语言，枚举值范围：zh 中文，en 英文。默认为en。|

## 返回参数 {#section_wdq_fwn_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 {#section_vwy_lwn_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|该域名存在正在处理中的操作，请稍后再试。|

## 示例 {#section_ebr_pwn_c2b .section}

**请求示例**

``` {#codeblock_zvt_ec4_4cz}
http://domain-intl.aliyuncs.com/?Action=SaveSingleTaskForCreatingOrderRedeem
&CurrentExpirationDate=0000
&DomainName=test.com
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_hha_bgh_i2t}
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveSingleTaskForCreatingOrderRedeemResponse>
        <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
        <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
    </SaveSingleTaskForCreatingOrderRedeemResponse>
    ```

-   JSON示例

    ``` {#codeblock_xae_9at_dkr}
    {    
      "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
      "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
    }
    ```


