# TransferInReenterTransferAuthorizationCode {#concept_w33_qrp_b2b .concept}

TransferInReenterTransferAuthorizationCode：域名转入重新输入转移密码。

## 请求参数 {#section_m4v_3kr_b2b .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|DomainName|String|是|test.com|域名。|
|TransferAuthorizationCode|String|是|testCode|转移密码。|
|Lang|String|否|en|接口返回信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_ufg_tkr_b2b .section}

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|唯一请求识别码。|

## 示例 {#section_of5_424_b2b .section}

**请求示例**

``` {#codeblock_4g4_7nu_53f}
/?Action=TransferInReenterTransferAuthorizationCode
&DomainName=test.com
&TransferAuthorizationCode=testCode
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_tr8_5qe_9qi}
    <TransferInReenterTransferAuthorizationCodeResponse>
      <RequestId>A8734DAA-56BB-4181-825E-8EE1F0C85DF4</RequestId>
    </TransferInReenterTransferAuthorizationCodeResponse>
    ```

-   JSON示例

    ``` {#codeblock_8e3_1wh_edm}
    {
        "RequestId":"F7C42D02-2FBE-475A-85A2-872865926EDC"
    }
    ```


**异常返回示例**

-   XML示例

    ``` {#codeblock_k9n_o0h_is2}
    <Error>
      <RequestId>F367C925-88F9-4297-A604-0ACDD1E8D5D4</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>DomainTransferPendingNotExist</Code>
      <Message>The domain name is not currently being transferred in.</Message>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_1vh_r3b_g4t}
    {
        "Code":"DomainTransferPendingNotExist",
        "HostId":"domain.aliyuncs.com",
        "Message":"The domain name is not currently being transferred in.",
        "RequestId":"20E291F8-A08C-4999-93B8-5C16B8F49B87"
    }
    ```


## 错误码 {#section_nwb_424_b2b .section}

[单击查看本产品错误码](intl.zh-CN/API 参考/附录/错误代码表.md#)。

