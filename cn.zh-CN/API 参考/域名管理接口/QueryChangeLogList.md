# QueryChangeLogList {#concept_ptg_qyk_c2b .concept}

QueryChangeLogList：分页查询自己账户下的操作日志。

## 请求参数 {#section_b1f_xrl_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：QueryChangeLogList。|
|PageNum|Integer|是|分页页码，最小值1。|
|PageSize|Integer|是|分页大小，最小值1，最大值100。|
|StartDate|Long|否|操作日期范围查询开始时间，UTC时间1970年1月1日0点距离现在的毫秒数。|
|EndDate|Long|否|操作日期范围查询结束时间，UTC时间1970年1月1日0点距离现在的毫秒数。|
|DomainName|String|否|待查询操作日志的域名。|
|Lang|String|否|接口返回信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|

## 返回参数 {#section_tlk_1sl_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TotalItemNum|Integer|记录总数。|
|CurrentPageNum|Integer|当前页码。|
|TotalPageNum|Integer|总页数。|
|PageSize|Integer|分页大小。|
|PrePage|Boolean|是否有上一页。|
|NextPage|Boolean|是否有下一页。|
|ResultLimit|Boolean|当前查询除分页限制外，服务端最多处理最近1000条记录。如结果超过1000条，ResultLimit为true，请缩小时间范围重新搜索；否则ResultLimit为false。|
|Data|[ChangeLogType](#table_u4w_fsl_c2b)|操作日志列表。|

|名称|类型|描述|
|:-|:-|:-|
|DomainName|String|域名|
|Result|String|操作结果|
|Operation|String|操作行为|
|OperationIPAddress|String|操作IP|
|Details|String|详情|
|Time|String|操作时间，UTC时间，如2017-12-25 12:00:00，具体格式与入参Lang有关。|

## 错误码 {#section_lvw_ksl_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_wll_2tl_c2b .section}

**请求示例**

``` {#codeblock_eqq_758_8ah}
http://domain-intl.aliyuncs.com/?Action=QueryChangeLogList
&PageNum=1
&PageSize=1
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_og6_ifi_9ld}
    <?xml version='1.0' encoding='UTF-8'?>
    <QueryChangeLogListResponse>
        <Data>
            <ChangeLog>
                <Result>Failed</Result>
                <Operation>DNS modification</Operation>
                <Time>2017-12-26 12:00:00</Time>
                <Details>dns1;dns2 -> dns3;dns4</Details>
                <DomainName>test1.com</DomainName>
                <OperationIPAddress>127.0.0.1</OperationIPAddress>
            </ChangeLog>
        </Data>
        <TotalItemNum>1000</TotalItemNum>
        <PageSize>1</PageSize>
        <CurrentPageNum>1</CurrentPageNum>
        <RequestId>2DEDFF32-7827-46B1-BE90-3DB8ABD91A58</RequestId>
        <PrePage>false</PrePage>
        <TotalPageNum>1000</TotalPageNum>
        <ResultLimit>true</ResultLimit>
        <NextPage>true</NextPage>
    </QueryChangeLogListResponse>
    ```

-   JSON示例

    ``` {#codeblock_857_v0m_0pw}
    {
      "currentPageNum": 1,
      "data": [
        {
          "details": "dns1;dns2 -> dns3;dns4",
          "domainName": "test1.com",
          "operation": "DNS modification",
          "operationIPAddress": "127.0.0.1",
          "result": "Failed",
          "time": "2017-12-26 12:00:00"
        }
      ],
      "nextPage": true,
      "pageSize": 1,
      "prePage": false,
      "requestId": "0B83F967-7135-49A3-B249-ABC14CBA6B8B",
      "resultLimit": true,
      "totalItemNum": 1000,
      "totalPageNum": 1000
    }
    ```


