# Domain security FAQs {#concept_ixj_3vd_b2b .concept}

-   [Will I be charged for domain name proxy?](#section_01)
-   [What should I do if I want to modify domain name information when the domain name security lock has been set?](#section_02)
-   [Is the domain name lock effective when the domain name expires?](#section_03)
-   [What is the diagnosing and processing scheme for DNS hijacking?](#section_04)
-   [Is verification by phone needed for domain name resolution?](#section_05)
-   [What can I do if the domain name is stolen?](#section_vkv_1wd_b2b)

## Will I be charged for domain name proxy? {#section_01 .section}

The domain name proxy service is a free service. You can enable domain name proxy for domain names registered with Alibaba Cloud for free.

However, domain names using a registrant other than Alibaba Cloud are charged for this service.

To comply with ICANN’s Temporary Specification for gTLD Registration Data and the European Union’s General Data Protection Regulation \(GDPR\), our registrar’s public WHOIS output no longer displays personal data from 25 May 2018. As your privacy is protected by default after the change becomes effective, Privacy & Proxy Service provided by Alibaba Cloud is suspended after 25 May 2018.

## What should I do if I want to modify domain name information when the domain name security lock has been set? {#section_02 .section}

When the domain name security lock is enabled, you must temporarily disable it to modify the domain name information.

**Note:**After modifying the domain name information, restore the domain name lock in time.

For more information about domain name lock service, see [set domain name security lock](../../../../../intl.en-US/Domain security FAQs/Update prohibition lock service.md#).

## Is the domain name lock effective when the domain name expires? {#section_03 .section}

No. The domain name lock is dependent on the domain name, so expiration time for the domain name lock is no later than that of the domain name. When the domain name expires, the domain name lock service is automatically disabled.

When you renew or redeem the domain name, you can also re-enable the domain name lock service.

For more information about domain name lock service, see [set domain name security lock](../../../../../intl.en-US/Domain security FAQs/Update prohibition lock service.md#).

## What is the diagnosing and processing scheme for DNS hijacking? {#section_04 .section}

DNS is used for domain name resolution. When a domain name is used to access a website or corresponding service, it must be resolved by DNS to a corresponding IP address \(the server\), so that the Internet can route the domain name to a proper node and return the expected content to the user.

DNS hijacking intercepts a domain name resolution request \(based on the purpose of hijacking\) within a specific network range \(a local area or a whole network\) and returns a wrong IP address or does not respond, so that the real user accesses an incorrect service or false information.

The diagnosing and processing scheme for DNS hijacking is as follows:

-   Run mslookup \(for a Windows host\) or dig \(for a Linux host\) on the local machine to check whether the resolved IP address is correct.
-   Use external tools to collect and confirm failure details such as hijacking range.
-   Feed back the test result to corresponding ISP for handling as soon as possible, and try to modify the DNS to Alibaba Cloud DNS \(223.5.5.5 or 223.6.6.6\) to check whether the resolution is normal.
-   For emergency businesses, you can directly access through IP addresses.

## Is verification by phone needed for domain name resolution? {#section_05 .section}

When you perform resolution operations in the Member Center, you may be required to enter the phone verification code, indicating that you are not operating in a commonly used computer or network environment, and a risk control is triggered.

If your phone number is normal while you cannot receive the verification code, try the following methods:

-   The verification code may be delayed. If you still cannot receive the verification code after waiting for a while, you can try again later.
-   Confirm whether your phone can send and receive text messages \(such as whether your phone charge is overdue\).
-   Check whether the verification message is intercepted by third-party security apps \(such as 360 Mobile Guard\).
-   If none of the preceding methods works, replace the SIM card to another phone and try again.

## What can I do if the domain name is stolen? {#section_vkv_1wd_b2b .section}

If the domain name is managed in Alibaba Cloud before it is stolen, we do our best to help you retrieve the stolen domain name. Domain name theft is generally divided into two situations:

-   The domain name is stolen, but still being managed in Alibaba Cloud.

    -   Call after-sales to contact us as soon as possible, to take measures such as locking the domain name, to prevent the domain name from being transferred out or the domain information being modified.
    -   At the same time you must provide materials that can prove the identity of the registrant to Alibaba Cloud.
-   The domain name is stolen, and it is transferred out of Alibaba Cloud and managed by another registrar.

    -   Contact Alibaba Cloud.

        You must contact Alibaba Cloud promptly when the domain name is stolen, and provide detailed feedback, so that Alibaba Cloud can respond in time. You can ask Alibaba Cloud to contact the current registrar to help lock the domain name and prevent the domain name from being transferred again or the domain information being modified.

    -   Contact the current registrar.

        You can ask Alibaba Cloud to contact the current registrar, or you can contact the current registrar by yourself, to report and provide evidence of the stolen domain name. When the current domain name service provider receives the report, it generally informs the domain name certification materials to be provided within 3 working days, including the registrant’s certificate materials and a retrieve statement. International registrars require evidence and statement in English.

    -   Wait for the current registrar’s investigation.

        The current registrar reviews and starts a investigation after receiving your evidentiary materials. The investigation generally takes a week. If investigation result from the current registrar shows a malicious transfer, Alibaba Cloud creates an account with the current registrar for the current registrar to transfer the stolen domain name to.

    -   Retrieve the stolen domain name. You can contact Alibaba Cloud to obtain the newly created account of the current registrar, to regain the domain name registrant. You can either keep the domain name in this account, or transfer it back to Alibaba Cloud.


