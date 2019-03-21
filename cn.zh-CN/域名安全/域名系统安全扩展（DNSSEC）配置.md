# 域名系统安全扩展（DNSSEC）配置 {#concept_szx_dqd_3gb .concept}

域名系统安全扩展（DNS Security Extensions，DNSSEC）是用于确定源域名可靠性的数字签名 ，通过添加DNSSEC记录到域名，可以增强对DNS域名服务器的身份认证，进而帮助防止DNS缓存污染等攻击。本文介绍如何在阿里云域名服务控制台上添加、同步DNSSEC记录。

## DNSSEC设置限制 {#section_odg_y45_jgb .section}

-   域名后缀类型：

    阿里云还未全面支持所有后缀类型域名的DNSSEC设置，目前支持.com/.net/.cc/.tv/.name/.info/.mobi/.pro/.xin/.biz/.club等域名的DNSSEC设置，不支持DNSSEC设置的域名在其控制台中无**DNSSEC设置**入口。实际支持情况以控制台左侧菜单显示为准。

-   域名解析渠道：

    使用非阿里云解析服务进行DNS解析的域名，可以按照如下步骤设置和查看DNSSEC。使用阿里云解析服务进行DNS解析的域名暂无法成功的进行DNSSEC设置操作。


## 操作步骤 {#section_ivq_4n5_jgb .section}

1.  登录 [阿里云域名控制台](https://netcn.console.aliyun.com/core/domain/list)，在相应域名后面单击 **管理**。
2.  在左侧导航栏的**域名列表**中，找到待配置的域名，在**操作**列单击**管理**。
3.  在弹出的页面中单击**DNSSEC设置**，进入DNSSEC设置页面。

    **说明：** 不支持DNSSEC设置的域名，进入操作列表后，左侧无**DNSSEC设置**操作入口。

4.  （可选）单击**同步DS记录**。

    如果此域名是从其他域名注册商转入阿里云，且在原注册商处添加过DNSSEC记录，可单击**同步DS记录**，将之前添加的DNSSEC记录同步至阿里云控制台。

5.  单击**添加DS记录**添加新的DNSSEC记录。

    **说明：** 每个域名最多添加8条DNSSEC记录。

6.  在弹出的页面中填写参数信息，填写完成确认无误后单击**提交**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/85415/155315305036516_zh-CN.png)

7.  在弹出的窗口中单击**获取验证码**，收到验证码后填写人输入框中，完成短信的验证码安全验证。

