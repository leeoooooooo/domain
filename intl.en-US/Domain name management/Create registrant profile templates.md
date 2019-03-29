# Create registrant profile templates {#concept_ibb_vbw_12b .concept}

Domain name registration, transfer, and trading require a registrant profile, including the registrant type, contact email, phone number, and address. Alibaba Cloud Domain allows you to create templates to manage registrant profiles.

We recommend that you decide the registrant of the domain name, create a registrant profile, and complete the real-name authentication process before you register, transfer, or trade a domain name.

## Template description {#section_gs1_311_ygb .section}

Alibaba Cloud Domain allows you to create two types of templates: common templates and CNNIC templates. You can use these templates to register domain names and change registrants.

|Template type|Scenario|Notes|
|:------------|:-------|:----|
|Common template|You can use a common template to register domain names, transfer domain names, and change registrants. This template cannot be applied to domain names that use the following top-level domains: .cn, .中国, .公司, and .网络.|The email address of the registrant must be verified after a common template is created. Otherwise, you cannot use the template to register a domain name.|
|CNNIC template|You can use a CNNIC template to register domain names, transfer domain names, and change registrants. This template can only be applied to domain names that use the following top-level domains: .cn, .中国, .公司, and .网络. You can also use a CNNIC template to complete the real-name authentication process.| -   The email address of the registrant must be verified after a CNNIC template is created. Otherwise, you cannot use the template to register a domain name.
-   You must complete the real-name authentication process after a CNNIC template is created. Otherwise, .cn, .中国, .公司, and .网络 domain names that you have registered using the template will be in **Serverhold** status and become inaccessible.

 |

## Create a common template {#section_cmq_321_ygb .section}

You can create a **common template** on the Registrant Profiles page in the console or when you register a domain name.

You must select a template when you register a domain name. If you have not created a template, perform the following steps to create a **common template** in the Alibaba Cloud Domain console.

1.  Log on to the [Alibaba Cloud Domain console](https://dc.console.aliyun.com/) and click Registrant Profiles.
2.  Click **Common template** and then click **Create Registrant Profile** in the upper-right corner.
3.  Enter all required information and click **Save**.

    **Note:** The information that you entered must be complete, real, and legal.

4.  Verify the email address

    After you create a **common template**, click **Verify Now** to verify the email address of the registrant. You must provide a real and valid email address as ICANN requires.


On the Registrant Profiles page, you can perform the following operations on an existing template:

-   **Set as default**: sets the template as the default template for registering domain names.
-   **Delete**: deletes the template.
-   **View**: displays details of the registrant.

## Create a CNNIC template {#section_ftz_211_ygb .section}

You can create a **CNNIC template** on the Registrant Profiles page in the console, or when you register a .cn domain name.

You must select a template when you register a domain name. If you have not created a template, perform the following steps to create a **CNNIC template** in the Alibaba Cloud Domain console.

1.  Log on to the [Alibaba Cloud Domain console](https://dc.console.aliyun.com/) and click Registrant Profiles.
2.  Click **CNNIC template** and then click **Create Registrant Profile** in the upper-right corner.
3.  Select a **registrant type**, enter all required information, and click **Save**.

    **Note:** The information that you entered must be complete, real, and legal.

4.  Verify the email address

    After you create a **CNNIC template**, click **Verify Now** to verify the email address of the registrant. You must provide a real and valid email address as ICANN requires.

5.  Real-name authentication

    After you create a **CNNIC template**, you must complete the real-name authentication process for the **CNNIC template**. For more information, see [Real-name authentication for .cn templates](../../../../../intl.en-US/Real-name authentication for domains /Real-name authentication for .cn domains.md#section_rdn_q41_ygb).


On the Registrant Profiles page, you can perform the following operations on an existing template:

-   **Set as default**: sets the template as the default template for registering domain names.
-   **Delete**: deletes the template.
-   **View**: displays details of the registrant.

