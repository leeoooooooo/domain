# SubmitEmailVerification {#concept_s3f_2mr_b2b .concept}

SubmitEmailVerification：按照ICANN政策规则，域名持有人邮箱必须经过真实性验证，可通过此接口提交Email邮箱验证。

## 请求参数 {#section_wy4_pmr_b2b .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SubmitEmailVerification。|
|Email|String|是|邮箱 多个使用逗号（,）分隔。|
|SendIfExist|Boolean|是|记录已经存在时是否继续发送。|
|Lang|String|否|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|

## 返回参数 {#section_u1p_wmr_b2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|SuccessList|[SendResultType](#table_ecg_2nr_b2b)|发送成功列表。|
|FailList|[SendResultType](#table_ecg_2nr_b2b)|发送失败列表。|
|ExistList|[SendResultType](#table_ecg_2nr_b2b)|已经存在列表。|

|名称|类型|描述|
|:-|:-|:-|
|Email|String|验证邮箱|
|Code|String|返回code|
|Message|String|返回信息|

## 错误码 {#section_tmt_ynr_b2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_lpr_34r_b2b .section}

**请求示例**

``` {#codeblock_4s7_5rq_v19}
http://domain-intl.aliyuncs.com/
?Action=SubmitEmailVerification
&InstanceId=ST2017120814571100001303
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_dc9_3kg_lv0}
    <?xml version='1.0' encoding='UTF-8'?>
    <SubmitEmailVerificationResponse>
        <FailList>
            <SendResult>
                <Email>aaa@test.com</Email>
                <Message>The maximum number of attempts allowed to send the email
                    verification link is exceeded.
                </Message>
                <Code>SendTokenQuotaExceeded</Code>
            </SendResult>
        </FailList>
        <RequestId>E2A8A5EF-DF8A-4C48-8FD4-9F6BD71AB26D</RequestId>
        <ExistList />
        <SuccessList>
            <SendResult>
                <Email>ccc@test.com</Email>
                <Message />
                <Code />
            </SendResult>
            <SendResult>
                <Email>ddd@test.com</Email>
                <Message />
                <Code />
            </SendResult>
        </SuccessList>
    </SubmitEmailVerificationResponse>
    ```

-   JSON示例

    ``` {#codeblock_s9r_wd6_ur2}
    {
      "existList": [
        {
          "email": "aaa@test.com"
        }
      ],
      "failList": [
        {
          "code": "SendTokenQuotaExceeded",
          "email": "bbb@test.com",
          "message": "The maximum number of attempts allowed to send the email verification link is exceeded."
        }
      ],
      "requestId": "2EF65AFD-A2C4-48D3-B326-ACB52B5A6771",
      "successList": [
        {
          "email": "ccc@test.com"
        },
        {
          "email": "ddd@test.com"
        }
      ]
    }
    ```


