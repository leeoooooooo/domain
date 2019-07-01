# TransferInRefetchWhoisEmail {#concept_dy3_prp_b2b .concept}

TransferInRefetchWhoisEmail：当域名转入进行邮箱验证，系统自动获取whois上持有者邮箱不对或者无法获取到邮箱时，重新抓取whois邮箱。

## 请求参数 {#section_ymj_42r_b2b .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|DomainName|String|是|test.com|域名。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_ksw_pjr_b2b .section}

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|唯一请求识别码。|

## 示例 {#section_of5_qbr_b2b .section}

**请求示例**

``` {#codeblock_4zp_ouj_t16}
/?Action=TransferInRefetchWhoisEmail
&DomainName=test.com
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_a7m_vzm_khc}
    <TransferInRefetchWhoisEmailResponse>
      <RequestId>9625281F-1176-4F57-ACBB-3AEF6E407AFE</RequestId>
    </TransferInRefetchWhoisEmailResponse>
    ```

-   JSON示例

    ``` {#codeblock_3fv_klf_93m}
    {
        "RequestId":"C01181CC-D03C-465F-B89F-C78B721567D0"
    }
    ```


**异常返回示例**

-   XML示例

    ``` {#codeblock_cv0_gyx_7jv}
    <Error>
      <RequestId>7618A307-69AD-4CC4-BC44-A898DB4FD9F4</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>DomainTransferPendingNotExist</Code>
      <Message>The domain name is not currently being transferred in.</Message>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_txb_wbq_w54}
    {
        "Code":"DomainTransferPendingNotExist",
        "HostId":"domain.aliyuncs.com",
        "Message":"The domain name is not currently being transferred in.",
        "RequestId":"B94591C4-3F8F-4EDB-BE09-DEBC8837D513"
    }
    ```


## 错误码 {#section_nwb_44cr_b2b .section}

[单击查看本产品错误码](intl.zh-CN/API 参考/附录/错误代码表.md#)。

