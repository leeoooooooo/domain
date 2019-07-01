# ListEmailVerification {#concept_k4m_njq_b2b .concept}

ListEmailVerification：分页查询自己账户下的邮箱验证列表。

## 请求参数 {#section_bl4_fll_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：ListEmailVerification。|
|PageNum|Integer|是|分页页码。|
|PageSize|Integer|是|分页大小。|
|BeginCreateTime|Long|否|验证日期范围查询开始时间，UTC时间1970年1月1日0点距离现在的毫秒数。|
|EndCreateTime|Long|否|验证日期范围查询结束时间，UTC时间1970年1月1日0点距离现在的毫秒数。|
|Email|String|否|待查询验证的邮箱。|
|VerificationStatus|Integer|否|验证状态，枚举值：0 等待验证；1 验证成功。|
|Lang|String|否|接口返回信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|

## 返回参数 {#section_5eb_6y3_fm7 .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TotalItemNum|Integer|域名总数。|
|CurrentPageNum|Integer|当前页码。|
|TotalPageNum|Integer|总页数。|
|PageSize|Integer|分页大小。|
|PrePage|Boolean|是否有上一页。|
|NextPage|Boolean|是否有下一页。|
|Data|[EmailVerificationType](#table_tsy_4ll_c2b)|邮箱验证列表。|

|名称|类型|描述|
|:-|:-|:-|
|GmtCreate|String|创建时间|
|GmtModified|String|更新时间|
|Email|String|验证邮箱|
|UserId|String|用户ID|
|EmailVerificationNo|String|邮箱验证编号|
|TokenSendTime|String|邮箱验证Token发送时间|
|VerificationStatus|Integer|邮箱验证状态。枚举值：0 等待验证；1 验证成功|
|VerificationTime|String|邮箱验证确认时间|
|SendIp|String|邮箱验证发送IP|
|ConfirmIp|String|邮箱验证确认IP|

## 错误码 {#section_gn7_x2t_0np .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_sff_1ml_c2b .section}

**请求示例**

``` {#codeblock_mj4_7a6_kaw}
http://domain-intl.aliyuncs.com/
?Action=ListEmailVerification
&PageNum=1
&PageSize=1
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_afx_8ni_pht}
    <?xml version='1.0' encoding='UTF-8'?>
    <ListEmailVerificationResponse>
        <Data>
            <EmailVerification>
                <ConfirmIp>127.0.0.1</ConfirmIp>
                <TokenSendTime>Dec 25,2017 03:38:46</TokenSendTime>
                <Email>test1@aliyun.com</Email>
                <VerificationStatus>1</VerificationStatus>
                <SendIp>127.0.0.1</SendIp>
                <VerificationTime>Dec 25,2017 03:41:11</VerificationTime>
                <EmailVerificationNo>00000a21fd374da99d9c95b48500000</EmailVerificationNo>
                <UserId>0000</UserId>
                <GmtCreate>Dec 25,2017 03:38:46</GmtCreate>
                <GmtModified>Dec 25,2017 03:41:11</GmtModified>
            </EmailVerification>
            <EmailVerification>
                <ConfirmIp>127.0.0.1</ConfirmIp>
                <TokenSendTime>Dec 25,2017 03:35:22</TokenSendTime>
                <Email>test2@aliyun.com</Email>
                <VerificationStatus>1</VerificationStatus>
                <SendIp>127.0.0.1</SendIp>
                <VerificationTime>Dec 25,2017 03:36:57</VerificationTime>
                <EmailVerificationNo>0000021fd374da99d9c95b48500000</EmailVerificationNo>
                <UserId>0000</UserId>
                <GmtCreate>Dec 25,2017 03:32:40</GmtCreate>
                <GmtModified>Dec 25,2017 03:36:57</GmtModified>
            </EmailVerification>
        </Data>
        <TotalItemNum>2</TotalItemNum>
        <PageSize>500</PageSize>
        <CurrentPageNum>1</CurrentPageNum>
        <RequestId>4BF41EC0-C147-4F88-8B3D-D569AF5C3E8B</RequestId>
        <PrePage>false</PrePage>
        <TotalPageNum>1</TotalPageNum>
        <NextPage>false</NextPage>
    </ListEmailVerificationResponse>
    ```

-   JSON示例

    ``` {#codeblock_3h5_i6w_vrw}
    {
      "currentPageNum": 1,
      "data": [
        {
          "confirmIp": "127.0.0.1",
          "email": "test1@aliyun.com",
          "emailVerificationNo": "00000a21fd374da99d9c95b48500000",
          "gmtCreate": "Dec 25,2017 03:38:46",
          "gmtModified": "Dec 25,2017 03:41:11",
          "sendIp": "127.0.0.1",
          "tokenSendTime": "Dec 25,2017 03:38:46",
          "userId": "0000",
          "verificationStatus": 1,
          "verificationTime": "Dec 25,2017 03:41:11"
        },
        {
          "confirmIp": "127.0.0.1",
          "email": "test2@aliyun.com",
          "emailVerificationNo": "0000021fd374da99d9c95b48500000",
          "gmtCreate": "Dec 25,2017 03:32:40",
          "gmtModified": "Dec 25,2017 03:36:57",
          "sendIp": "127.0.0.1",
          "tokenSendTime": "Dec 25,2017 03:35:22",
          "userId": "0000",
          "verificationStatus": 1,
          "verificationTime": "Dec 25,2017 03:36:57"
        }
      ],
      "nextPage": false,
      "pageSize": 500,
      "prePage": false,
      "requestId": "09D3DA75-B3B5-480B-9100-92DC43919B46",
      "totalItemNum": 2,
      "totalPageNum": 1
    }
    ```


