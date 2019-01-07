# 验证邮箱Token {#concept_yhk_mrp_b2b .concept}

验证邮箱Token。

## 请求参数 {#section_cbr_jtq_b2b .section}

公共请求参数，请参见[公共参数](intl.zh-CN/API 参考（推荐版）/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：VerifyEmail。|
|Token|String|是|邮箱中收到的Token。|
|Lang|String|否|接口返回信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|

## 返回参数 {#section_szd_stq_b2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|

## 错误码 {#section_itv_5tq_b2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_jmz_wtq_b2b .section}

**请求示例**

```
http://domain-intl.aliyuncs.com/?Action=VerifyEmail
&Email=test@aliyun.com
&<公共请求参数>
```

**返回示例**

-   XML示例

    ```
    <?xml version='1.0' encoding='UTF-8'?>
    <VerifyEmailResponse>
        <RequestId>FD3AD289-83EE-4E32-803A-CF1B3A8EEE64</RequestId>
    </VerifyEmailResponse>
    ```

-   JSON示例

    ```
    {
        "requestId":"6ED795BD-192E-4921-B8E5-1BCA6F71186C"
    }
    ```


