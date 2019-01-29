# Configure DNS Security Extensions {#concept_szx_dqd_3gb .concept}

DNS Security Extensions \(DNSSEC\) provides you with digital signatures to verify the destinations URLs that your domain names are redirected to. You can add DNSSEC records to a domain name to authenticate the DNS servers that host your domain name. This helps you avoid attacks such as DNS cache poisoning. This section describes how to add and replicate DNSSEC records to the Alibaba Cloud Domain console.

## Restrictions on DNSSEC configurations {#section_odg_y45_jgb .section}

-   Supported types of top-level domains:

    Currently, Alibaba Cloud does not support DNSSEC for all top-level domains. Supported top-level domains include .com, .net, .cc, .tv,. name, .info, .mobi, .pro, .xin, .biz, and .club. The **DNSSEC Setting** tab will not be displayed in the left-side navigation pane if a domain name does not support DNSSEC. The DNSSEC Setting tab will be displayed in the left-side navigation pane if a domain name supports DNSSEC.

-   DNS resolution:

    You can follow the procedure in the following section to configure and view DNSSEC of domain names that are not translated by Alibaba Cloud DNS. Currently, you cannot configure DNSSEC for domain names that are translated by Alibaba Cloud DNS.


## Procedure {#section_ivq_4n5_jgb .section}

1.  Log on to the [Alibaba Cloud Domain console](https://netcn.console.aliyun.com/core/domain/list) and click **Manage** in the Actions column of the specified domain name.
2.  In the left-side navigation pane, click **Domain Names**, locate the specified domain name, and click **Manage** in the **Actions** column.
3.  On the dialog box that appears, click **DNSSEC Setting** to go to the DNSSEC Setting page.

    **Note:** The **DNSSEC Setting** tab will not be displayed in the left-side navigation pane of this dialog box if the domain name does not support DNSSEC.

4.  \(Optional\) Click **Synchronize DS Record**.

    If the domain name is transferred to Alibaba Cloud from another domain name registrar and you have previously added DNSSEC records, click **Synchronize DS Record** to replicate the DNSSEC records to the Alibaba Cloud Domain console.

5.  Click **Add DS Record** to add a DNSSEC record.

    **Note:** You can add up to eight DNSSEC records to a domain name.

6.  In the dialog box that appears, enter the required information correctly and click **Submit**.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/85415/154875083836516_en-US.png)

7.  In the dialog box that appears, click **Get Verification Code** to obtain a verification code, and enter the code in the input field to complete the email verification process.

