# QueryRegistrantProfiles {#concept_l4w_rzb_b2b .concept}

查询自己账户下的域名信息模板。

## 请求参数 {#section_dxl_j1c_b2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：QueryRegistrantProfiles。|
|RegistrantOrganization|String|否|域名持有者名称。|
|RegistrantProfileId|Long|否|联系人模板ID。|
|DefaultRegistrantProfile|Boolean|否|是否默认模板。|
|PageNum|Integer|否|分页的页码。|
|PageSize|Integer|否|分页的每页记录数。|

## 返回参数 {#section_nxv_w1c_b2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TotalItemNum|Integer|总记录数。|
|CurrentPageNum|Integer|当前页码。|
|TotalPageNum|Integer|总页码。|
|PageSize|Integer|每页的记录数。|
|PrePage|Boolean|是否有上一页。|
|NextPage|Boolean|是否有下一页。|
|RegistrantProfile|[RegistrantProfileType](intl.zh-CN/API 参考/信息模板接口/QueryRegistrantProfiles.md#table_s4s_tmq_b2b)|域名信息模板列表。请参见下表：RegistrantProfileType。|

|名称|类型|描述|
|:-|:-|:-|
|RegistrantProfileId|Long|域名信息模板ID|
|CreateTime|String|创建时间|
|UpdateTime|String|更新时间|
|Telephone|String|电话|
|DefaultRegistrantProfile|Boolean|是否默认模板|
|Country|String|国家代码 如CN，US|
|Province|String|省份|
|TelArea|String|电话国家代码|
|City|String|城市|
|PostalCode|String|邮政编码|
|Email|String|Email|
|Address|String|具体的地址|
|RegistrantName|String|联系人名称|
|RegistrantOrganization|String|持有者名称|
|TelExt|String|电话分机|
|EmailVerificationStatus|Integer|邮箱验证状态。取值范围：0 未验证；1 已验证|

**错误码** 

|错误代码|描述|HTTP状态码|语义|
|----|--|-------|--|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_vgl_jbc_b2b .section}

**请求示例**

``` {#codeblock_w1x_fv2_6cs}
http://domain-intl.aliyuncs.com/?Action=QueryRegistrantProfiles
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_bkw_n8i_3u5}
    <?xml version='1.0' encoding='UTF-8'?>
    <QueryRegistrantProfilesResponse>
        <TotalItemNum>11</TotalItemNum>
        <PageSize>2</PageSize>
        <CurrentPageNum>1</CurrentPageNum>
        <RequestId>1200F9CE-0000-4C5F-86C2-F8CF3828670D</RequestId>
        <PrePage>false</PrePage>
        <RegistrantProfiles>
            <RegistrantProfile>
                <Telephone>11119999</Telephone>
                <DefaultRegistrantProfile>true</DefaultRegistrantProfile>
                <EmailVerificationStatus>0</EmailVerificationStatus>
                <UpdateTime>Dec 25,2017 03:21:59</UpdateTime>
                <Country>US</Country>
                <Province>qa</Province>
                <TelArea>010</TelArea>
                <City>us</City>
                <RegistrantProfileId>5170612</RegistrantProfileId>
                <PostalCode>010101</PostalCode>
                <Email>xxx@xxx.com</Email>
                <CreateTime>Dec 25,2017 03:20:30</CreateTime>
                <Address>aqqqq</Address>
                <RegistrantName>pop</RegistrantName>
                <RegistrantOrganization>popus-x</RegistrantOrganization>
            </RegistrantProfile>
            <RegistrantProfile>
                <Telephone>15600000000</Telephone>
                <DefaultRegistrantProfile>false</DefaultRegistrantProfile>
                <EmailVerificationStatus>0</EmailVerificationStatus>
                <UpdateTime>Nov 22,2017 09:20:40</UpdateTime>
                <Country>MO</Country>
                <Province>Beijing</Province>
                <TelArea>853</TelArea>
                <City>Beijing</City>
                <RegistrantProfileId>5049715</RegistrantProfileId>
                <PostalCode>100086</PostalCode>
                <Email>abctest@xx.com</Email>
                <CreateTime>Nov 22,2017 09:20:40</CreateTime>
                <Address>Chaoyang District</Address>
                <RegistrantName>lk</RegistrantName>
                <RegistrantOrganization>lk</RegistrantOrganization>
            </RegistrantProfile>
        </RegistrantProfiles>
        <TotalPageNum>6</TotalPageNum>
        <NextPage>true</NextPage>
    </QueryRegistrantProfilesResponse>
    ```

-   JSON示例

    ``` {#codeblock_fqc_4ld_yse}
    {
      "CurrentPageNum": 1,
      "NextPage": true,
      "PageSize": 2,
      "PrePage": false,
      "RegistrantProfiles": {
        "RegistrantProfile": [
          {
            "Address": "aqqqq",
            "City": "us",
            "Country": "US",
            "CreateTime": "Dec 25,2017 03:20:30",
            "DefaultRegistrantProfile": true,
            "Email": "a@xxx.com",
            "EmailVerificationStatus": 0,
            "PostalCode": "010101",
            "Province": "qa",
            "RegistrantName": "x",
            "RegistrantOrganization": "xxx",
            "RegistrantProfileId": 5170612,
            "TelArea": "010",
            "Telephone": "11119999",
            "UpdateTime": "Dec 25,2017 03:21:59"
          },
          {
            "Address": "xx District",
            "City": "Beijing",
            "Country": "MO",
            "CreateTime": "Nov 22,2017 09:20:40",
            "DefaultRegistrantProfile": false,
            "Email": "abctest@xxx.com",
            "EmailVerificationStatus": 0,
            "PostalCode": "100086",
            "Province": "Beijing",
            "RegistrantName": "lk",
            "RegistrantOrganization": "lk",
            "RegistrantProfileId": 5049715,
            "TelArea": "853",
            "Telephone": "15600000000",
            "UpdateTime": "Nov 22,2017 09:20:40"
          }
        ]
      },
      "RequestId": "8843D641-7520-4399-9FCC-BFB90C068E6F",
      "TotalItemNum": 11,
      "TotalPageNum": 6
    }
    ```


