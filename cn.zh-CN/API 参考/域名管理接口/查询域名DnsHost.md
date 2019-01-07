# 查询域名DnsHost {#concept_xwb_wjq_b2b .concept}

QueryDnsHost：查询域名 DNS host。

## 请求参数 {#section_kn5_xdm_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考（推荐版）/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：QueryDnsHost。|
|InstanceId|String|是|域名实例编号可通过查询域名列表接口（[QueryDomainList](intl.zh-CN/API 参考（推荐版）/域名管理接口/查询域名列表.md#)）获得。

|
|Lang|String|否|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为en。|

## 返回参数 {#section_s3t_g2m_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|DnsHostList|[DnsHostType](#table_gjw_k2m_c2b)|DNS host信息。|

|名称|类型|描述|
|:-|:-|:-|
|DnsName|String|域名|
|IpList|IpListType|IP地址列表|

## 错误码 {#section_gy3_r2m_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_lxh_52m_c2b .section}

**请求示例**

```
http://domain-intl.aliyuncs.com/?Action=QueryDnsHost
&InstanceId=ST2017120814571100001303
&<公共请求参数>
```

**返回示例**

-   XML示例

    ```
    <?xml version='1.0' encoding='UTF-8'?>
    <QueryDnsHostResponse>
        <DnsHostList>
            <DnsHost>
                <DnsName>ns3</DnsName>
                <IpList>
                    <ip>185.27.134.201</ip>
                    <ip>218.83.159.236</ip>
                </IpList>
            </DnsHost>
        </DnsHostList>
        <RequestId>18A313DD-3AF3-40AA-84F9-56BA45DC511F</RequestId>
    </QueryDnsHostResponse>
    ```

-   JSON示例

    ```
    {
      "dnsHostList": [
        {
          "dnsName": "ns3",
          "ipList": [
            "185.27.134.201",
            "218.83.159.236"
          ]
        }
      ],
      "requestId": "6A973B69-7B5F-4959-AA89-ED4010541D20"
    }
    ```


