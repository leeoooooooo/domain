# ResendEmailVerification {#concept_dhd_zyk_c2b .concept}

ResendEmailVerification：重新发送验证邮件。

## 请求参数 {#section_dbr_dzm_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：ResendEmailVerification。|
|Email|String|是|邮箱，多个使用（,）分隔。|
|Lang|String|否|接口返回信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|

## 返回参数 {#section_zp1_3zm_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|SuccessList|[SendResultType](#table_ltc_lzm_c2b)|成功列表。|
|FailList|SendResultType|失败列表。|

|名称|类型|描述|
|:-|:-|:-|
|Email|String|验证邮箱|
|Code|String|返回code|
|Message|String|返回信息|

## 错误码 {#section_n1h_rzm_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|------:|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_mdg_tzm_c2b .section}

**请求示例**

``` {#codeblock_1up_271_ja1}
http://domain-intl.aliyuncs.com/?Action=ResendEmailVerification
&Email=test1@aliyun.com,test2@aliyun.com
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_mph_dpj_561}
    <?xml version='1.0' encoding='UTF-8'?>
    <ResendEmailVerificationResponse>
        <FailList>
            <SendResult>
                <Email>test1@aliyun.com</Email>
                <Message>The maximum number of attempts allowed to send the email verification link is exceeded.</Message>
                <Code>SendTokenQuotaExceeded</Code>
            </SendResult>
            <SendResult>
                <Email>test2@aliyun.com</Email>
                <Message>The maximum number of attempts allowed to send the email verification link is exceeded.</Message>
                <Code>SendTokenQuotaExceeded</Code>
            </SendResult>
        </FailList>
        <RequestId>0EA54E99-DB48-4CE3-A099-6ED8E451B8AC</RequestId>
        <SuccessList/>
    </ResendEmailVerificationResponse>
    ```

-   JSON示例

    ``` {#codeblock_ikt_dg4_3bz}
    {
      "failList": [
        {
          "code": "SendTokenQuotaExceeded",
          "email": "test1@aliyun.com",
          "message": "The maximum number of attempts allowed to send the email verification link is exceeded."
        },
        {
          "code": "ParameterIllegall",
          "email": "test2@aliyun.com",
          "message": "Parameter error"
        }
      ],
      "requestId": "8D93B5EC-09D5-43C3-A5ED-AFBC6A98DDDF",
      "successList": []
    }
    ```


