# Whois信息显示调整FAQ和ICANN临时规范的常见问题 {#concept_hp2_tdw_12b .concept}

## 为什么WHOIS查询后的显示信息变化了？ {#section_n1q_xmx_12b .section}

ICANN（互联网名称与数字地址分配机构）于2018年5月17日公布《通用顶级域名注册数据临时规范（Temporary Specification for gTLD Registration Data）》，要求注册局和注册商对WHOIS查询服务的公开显示信息进行必要调整。此次调整是ICANN为应对2018年5月25日生效的欧盟《通用数据保护条例（GDPR）》所做出的调整。

更多关于ICANN临时规范，请访问：https://www.icann.org/news/announcement-2018-05-17-en

## WHOIS显示信息调整后有哪些具体变化？ {#section_o1q_xmx_12b .section}

为落实ICANN临时规范要求，自2018年5月25日起阿里云WHOIS查询公开信息中将不再显示域名注册人、管理联系人和技术联系人的个人数据，包括姓名、邮箱、电话、街道地址等。

## 阿里云对ICANN临时规范的实施范围是什么？出于何种考虑？ {#section_q3h_1jv_c2b .section}

阿里云采取的对应落实方案符合ICANN合规要求；同时，阿里云处理和展示域名注册数据的模式适用于全球用户，并未将欧盟或本国用户进行区分，目的在于使全球用户能够享受同等程度和质量的数据保护服务。

## 域名注册流程和用户提交的信息是否也会有所变化？ {#section_p1q_xmx_12b .section}

没有变化。此次调整只是对WHOIS查询所显示的域名注册信息进行调整，域名注册所需的信息和注册流程仍维持不变。

## 域名注册商之间的转移流程是否也会有所变化？ {#section_q1q_xmx_12b .section}

由于WHOIS公开信息将不再显示域名注册人及管理联系人邮箱，ICANN的转移政策自2018年5月25日起有所调整。主要变化包括:

1.  转入注册商（Gaining Registrar）由于无法通过WHOIS获取转移域名信息，不再需要取得授权确认信（FOA）
2.  域名注册人必须重新提交完整的注册数据给转入的新注册商，转入注册商必须确认并核实注册人提交的数据；在此情况下，转移政策中有关注册人变更（Change of Registrant）的流程将不再适用。

## 域名转出阿里云时，新注册商以不能获取转移联系人邮箱为由拒绝协助办理域名转入时，该怎么办？ {#section_zxz_sjv_c2b .section}

 根据ICANN的临时政策，由于转入方注册商无法通过公开WHOIS信息获得转出方注册商的域名注册信息，因此不再要求转入方从转移联系人处获得转入确认信（FOA）。ICANN临时规范对域名转移的调整自5月25日起生效，如果转入注册商还没有落实的话，建议您联系转入注册商了解这个最新政策。

## 今后我应该如何联系域名持有人/管理联系人/技术联系人？ {#section_s1q_xmx_12b .section}

阿里云注册域名，可以在WHOIS查询结果显示页面，以提交在线表格方式向域名持有人/管理联系人/技术联系人发送信息。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/14342/6318_zh-CN.png)

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/14342/6319_zh-CN.png)

## 我想获取完整WHOIS信息，应该如何处理？ {#section_t1q_xmx_12b .section}

如果您基于投诉维权等合法、正当目的，希望获得相关域名的完整WHOIS信息，请您通过有权机构或司法机关向阿里云调取完整的WHOIS信息，阿里云将依法予以配合。

您也可在向阿里云提交投诉举报的同时，提出要求获取完整WHOIS信息的要求，阿里云将通过审慎判断，确定是否支持您的请求。

国际站举报中心入口：[https://www.alibabacloud.com/report](https://www.alibabacloud.com/report)

## 阿里云提供的域名隐私保护服务是否可以继续使用？ {#section_u1q_xmx_12b .section}

鉴于2018年5月25日WHOIS显示信息调整措施上线后，域名的注册信息已得到默认保护，届时阿里云的域名隐私保护服务将同步暂停服务。

## 隐私保护服务何时可以重新开启？ {#section_drx_blv_c2b .section}

阿里云将根据ICANN及其社群对WHOIS显示信息相关问题的后续讨论和政策调整，以及代理和隐私服务的正式政策制定情况确定恢复服务的时间。

## 此次WHOIS显示信息调整是否是长期方案？ {#section_v1q_xmx_12b .section}

ICANN临时政策有效期不能超过12个月但其间ICANN可以对临时政策要求进行修改。此外，ICANN作为全球域名系统和域名根服务器系统的管理机构，目前仍在协调全球域名注册局、注册商和其他社群成员研究制定关于通用顶级域名注册信息收集和展示的共识政策（Consensus Policy）。阿里云作为ICANN委任的域名注册商，未来可能须根据ICANN临时政策的修改或新共识政策新的要求对WHOIS展示信息作进一步调整。

## 为什么第三方WHOIS平台仍可以查询阿里云域名注册联系人信息？ {#section_l43_hlv_c2b .section}

通过阿里云注册的域名，除.COM .NET等Verisign域名的WHOIS信息由阿里云直接按调整后的规则提供外，其他阿里云域名的WHOIS信息均由相应的注册局提供，并由各注册商自行决定在其WHOIS平台的显示信息内容。由于各注册局、注册商对于GDPR和WHOIS显示信息调整的落实方案与进度暂不统一，因此该等在第三方WHOIS平台如何显示，取决于对应的注册局和注册商政策。

通过阿里云注册的.COM .NET等Verisign域名，目前通过第三方WHOIS平台所能查询到的阿里云域名注册联系人信息均为缓存信息，最新查询结果中，已不再包括阿里云域名的注册联系人信息。

