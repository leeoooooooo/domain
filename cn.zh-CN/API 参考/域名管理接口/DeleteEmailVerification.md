# DeleteEmailVerification {#concept_ur1_mjq_b2b .concept}

DeleteEmailVerification：已经验证通过的邮箱，可进行删除；但删除后，该邮箱还需要重新进行验证。

## 请求参数 {#section_jtz_h4l_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：DeleteEmailVerification。|
|Email|String|是|邮箱，多个邮箱使用逗号（,）分隔。|
|Lang|String|否|接口返回信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|

## 返回参数 {#section_oyr_m4l_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|SuccessList|[SendResultType](#table_l15_q4l_c2b)|删除成功列表。|
|FailList|[SendResultType](#table_l15_q4l_c2b)|删除失败列表。|

|名称|类型|描述|
|:-|:-|:-|
|Email|String|验证邮箱|
|Code|String|返回code|
|Message|String|返回信息|

## 错误码 {#section_ecg_v4l_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_bhn_bpl_c2b .section}

**请求示例**

``` {#codeblock_d6o_z5i_ydh}
http://domain-intl.aliyuncs.com/
?Action=DeleteEmailVerification
&Email=test1@aliyun.com,test2@aliyun.com
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_upc_dg6_4kz}
    <?xml version='1.0' encoding='UTF-8'?>
    <DeleteEmailVerificationResponse>
        <FailList>
            <SendResult>
                <Email>test1@aliyun.com</Email>
                <Message>Parameter error</Message>
                <Code>ParameterIllegall</Code>
            </SendResult>
            <SendResult>
                <Email>test2@aliyun.com</Email>
                <Message>Parameter error</Message>
                <Code>ParameterIllegall</Code>
            </SendResult>
        </FailList>
        <RequestId>7A3D0E4A-0D4B-4BD0-90D7-A61DF8DD26AE</RequestId>
        <SuccessList/>
    </DeleteEmailVerificationResponse>
    ```

-   JSON示例

    ``` {#codeblock_igp_2oy_sef}
    {
      "failList": [
        {
          "code": "ParameterIllegall",
          "email": "test1@aliyun.com",
          "message": "Parameter error"
        }
      ],
      "requestId": "B862F011-5E61-4302-88BD-A4EAA5326140",
      "successList": [
        {
          "email": "test2@aliyun.com"
        }
      ]
    }
    ```


