# 查询商标词key {#reference_y1b_z2s_5fb .reference}

CheckDomainSunriseClaim：根据传入域名查询商标词key。

## 请求参数 {#section_rpr_lfs_5fb .section}

公共请求参数，详见 [公共参数](cn.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值： CheckDomainSunriseClaim。|
|DomainName|String|是|域名名称。|

## 返回参数 {#section_dcq_bgs_5fb .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|Result|Integer|结果。可能值：0 不是商标词或不处于claim期，1 sunrise期，2 claim期。|
|ClaimKey|String|商标词key。|

## 错误码 {#section_wds_xgs_5fb .section}

对于所有接口的通用性错误，请参考 [错误代码表](cn.zh-CN/API 参考/附录/错误代码表.md#)。

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|Failed|Query failed.|2000|查询失败。|
|QueryRegistryFailed|Query registry failed.|2001|查询注册局失败。|
|Busy|Server is busy, please try again later.|3000|系统忙。|
|InvaildParameter|The parameter is invaild.|4000|非法参数。|
|Unauthorized|The resource is unauthorized.|5000|用户无资源授权或者该API不支持RAM。|

## 示例 {#section_chh_whs_5fb .section}

**请求示例**

```
http://domain.aliyuncs.com/?Action=CheckDomainSunriseClaim
&DomainName=abc.xin
&<公共请求参数>
```

**返回示例**

-   XML示例

```
<CheckDomainSunriseClaim>
    <RequestId>BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1</RequestId>
    <Result>1</Result>
    <ClaimKey>2017092100/8/2/1/kDfu9htHGEx_y-LJ3XSlKMZ70000020001</ClaimKey>
</CheckDomainSunriseClaim>
```

-   JSON示例

```
{
    "RequestId": "BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1",
    "Result": 2,
    "ClaimKey": "2017092100/8/2/1/kDfu9htHGEx_y-LJ3XSlKMZ70000020001"
}
```


