# 域名查询商标词tmch信息 {#reference_j1p_jks_5fb .reference}

LookupTmchNotice：根据传入商标词key查询tmch信息。

## 请求参数 {#section_awy_rns_5fb .section}

公共请求参数，详见 [公共参数](cn.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：LookupTmchNotice。|
|ClaimKey|String|是|域名商标词key。|

## 返回参数 {#section_cy5_tbx_5fb .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码|
|Id|String|tmch的通知id|
|NotBefore|String|商标通知开始时间|
|NotAfter|String|商标通知结束时间|
|Label|String|商标标签|
|Claims|List|商标信息列表|
|MarkName|String|商标名称|
|GoodsAndServices|String|商标产品及服务信息|
|JurDesc|Object|法律信息|
|JurCC|String|所在地|
|Desc|String|描述|
|Holders|List|商标持有者信息|
|Entitlement|String|持有者名称|
|Org|String|组织|
|Addr|Object|地址|
|Cc|String|国家|
|Sp|String|省|
|City|String|市|
|Street|String|街道|
|Pc|String|邮编|
|Contacts|List|商标联系人列表|
|Type|String|类型|
|Name|String|姓名|
|Org|String|组织|
|Voice|String|电话|
|Fax|String|传真|
|Email|String|电子邮件|
|Addr|Object|地址|
|Cc|String|国家|
|Sp|String|省|
|City|String|市|
|Street|String|街道|
|Pc|String|邮编|
|ClassDescs|List|类型描述|
|ClassNum|Integer|类型编号|
|Desc|String|描述|

## 错误码 {#section_aj5_hgx_5fb .section}

对于所有接口的通用性错误，请参考 [错误代码表](cn.zh-CN/API 参考/附录/错误代码表.md#)。

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|Failed|Query failed.|2000|查询失败。|
|QueryRegistryFailed|Query registry failed.|2002|查询TMCHDB失败。|
|Busy|Server is busy, please try again later.|3000|系统忙。|
|InvaildParameter|The parameter is invaild.|4000|非法参数。|
|Unauthorized|The resource is unauthorized.|5000|用户无资源授权或者该API不支持RAM。|

## 示例 {#section_sc4_h4x_5fb .section}

请求示例

```
http://domain.aliyuncs.com/?Action=LookupTmchNotice
&ClaimKey=2017092100/8/2/1/kDfu9htHGEx_y-LJ3XSlKMZ70000020001
&<公共请求参数>
```

返回示例

-   XML示例

```
<tmchNotice>
    <id>f58a66080000000000205821776</id>
    <notBefore>2018-10-13T00:00:00.0Z</notBefore>
    <notAfter>2018-10-15T00:00:00.0Z</notAfter>
    <label>noted</label>
    <claims>
        <claim>
            <markName>POTED</markName>
            <holder entitlement="owner">
            <org>Whitcoulls 2011 Limited</org>
            <addr>
                <street>Level 5 131 Queen Street </street>
                <city>Auckland</city>
                <pc>1010</pc>
                <cc>NZ</cc>
            </addr>
            </holder>
            <scontact>
            <contact type="agent">
                <name>AJ Park</name>
                <org>AJ Park </org>
                <addr>
                    <street>Level 22, State Insurance Tower</street>
                    <street>1 Willis St</street>
                    <street>Wellington </street>
                    <city>Wellington</city>
                    <pc>6011</pc>
                    <cc>NZ</cc>
                </addr>
                <voice>+64.44738278</voice>
                <fax>+64.44723358</fax>
                <email>dns@ajpark.com</email>
            </contact>
            </contacts>
            <classDesc classNum="18">Leather and imitations
                of leather, and goods made of these materials and not included in
                other classes; animal skins, hides; trunks and travelling bags;
                umbrellas and parasols; walking sticks; whips, harness and saddlery.
            </classDesc>
            <classDesc classNum="35">Advertising; business
                management; business administration; office functions.
            </classDesc>
            <goodsAndServices>Class 9: Calculators; bags, coverings,
                containers, carriers and holders for mobile phones, personal handheld
                computers and notebooks; headphones; speakers; blank storage media;
                batteries. Class 16: Paper
            </goodsAndServices>
        </claim>
    </claims>
</tmchNotice>
```

-   JSON示例

```
{
"Claims":{
    "Claim":[
        {
            "GoodsAndServices":"Class 9: Calculators; bags, coverings, containers, carriers and holders for mobile phones",
            "Contacts":{
                "Contact":[
                    {
                        "Name":"AJ Park",
                        "Email":"dns@ajpark.com",
                        "Voice":"+64.44738278",
                        "Fax":"+64.44723358",
                        "Org":"AJ Park ",
                        "Addr":{
                            "Street":{
                                "Street":[
                                    "Level 22, State Insurance Tower",
                                    "1 Willis St",
                                    "Wellington "
                                ]
                            },
                            "Pc":"6011",
                            "Cc":"NZ",
                            "City":"Wellington"
                        }
                    }
                ]
            },
            "Holders":{
                "Holder":[
                    {
                        "Org":"Whitcoulls 2011 Limited",
                        "Addr":{
                            "Street":{
                                "Street":[
                                    "Level 5 131 Queen Street "
                                ]
                            },
                            "Pc":"1010",
                            "Cc":"NZ",
                            "City":"Auckland"
                        },
                        "Entitlement":"owner"
                    }
                ]
            },
            "JurDesc":{
                "JurCC":"NZ",
                "Desc":"New Zealand"
            },
            "ClassDescs":{
                "ClassDesc":[
                    {
                        "ClassNum":18,
                        "Desc":"Leather and imitations of leather, and goods made of "
                    },
                    {
                        "ClassNum":35,
                        "Desc":"Advertising; business management; business administration; office functions. "
                    }
                ]
            },
            "MarkName":"NOTED"
        }
    ]
},
"NotBefore":"2018-10-13T00:00:00.0Z",
"NotAfter":"2018-10-23T00:00:00.0Z",
"RequestId":"01C10C8E-0468-468C-BCD9-E709BDD0AE8F",
"Id":"f58a66080000000000205821776",
"Label":"noted"
```


