# Real-name authentication failures and solutions {#concept_x3m_zwv_12b .concept}

After you submit all required information for real-name authentication, Alibaba Cloud immediately submits the information to the China Internet Network Information Center \(CNNIC\) for verification. CNNIC will verify the submitted verification information and the domain name registration information for authenticity, consistency, and completeness. If the verification fails, you can troubleshoot any issues according to the solutions described in this topic.

## Invalid certificates or identity documents {#section_spz_gqk_5gb .section}

If the system displays the message **Verification failed due to invalid certificate**, you can troubleshoot the fault as follows

1.  Check whether the domain name holder has a special occupation.

    Individuals with special occupations, for example, military personnel and monks, cannot use the 18-digit resident identity card number for verification. We recommend that you use other identification documentation for the verification.

2.  Check whether the submitted verification information is consistent with the domain registration information.

    For example, if you select Organization Holder and Unified Social Credit Code Certificate, but upload a scanned copy of a business license, the submitted verification information and the domain registration information are inconsistent.

3.  Check whether you have submitted a correct and valid identity document or certificate.

    Individual domain holders must submit a scanned copy of their resident identity card or passport. Photo examples:

    -   [Resident identity card](intl.en-US/Real-name authentication for domains /Real-name authentication examples/Real-name authentication examples for individual domain holders.md#section_bjz_lh3_wgb)
    -   [Passport](intl.en-US/Real-name authentication for domains /Real-name authentication examples/Real-name authentication examples for individual domain holders.md#section_fln_sy3_wgb)
    Organization domain holders must submit a copy of the business license, unified social credit code certificate, organization code certificate, or other valid certificates. Photo examples:

    -   [Business license](intl.en-US/Real-name authentication for domains /Real-name authentication examples/Real-name authentication examples for organization domain holders.md#section_wsm_jf3_wgb)
    -   [Unified social credit code certificate](intl.en-US/Real-name authentication for domains /Real-name authentication examples/Real-name authentication examples for organization domain holders.md#section_bjh_pck_wgb)
    -   [Organization code certificate](intl.en-US/Real-name authentication for domains /Real-name authentication examples/Real-name authentication examples for organization domain holders.md#section_f4l_xrd_xgb)
    -   [Other certificates](intl.en-US/Real-name authentication for domains /Real-name authentication examples/Real-name authentication examples for organization domain holders.md#section_jlt_gqz_zgb)

## Inconsistent domain holder names {#section_dgw_jqk_5gb .section}

If the system displays the message **Verification failed due to inconsistent names in the verification and registration information**, you can troubleshoot the fault as follows

-   Check whether the name of the domain holder specified in the submitted verification information is consistent with that in the domain registration information. Pay close attention to Chinese characters with similar forms or pronunciations. Do not use abbreviated or shortened names.
-   The certificate type that you select must be consistent with the one that you upload. If you select the business license, you must submit a scanned copy of your business license.
-   The certificate number that is specified in the verification information must be consistent with that of the actual certificate. If you select the resident identity card, business license, or unified social credit code certificate, make sure that the certificate number you specify in the verification information is consistent with that of the actual certificate.

    **Note:** 

    -   Use half-width characters when you enter the certificate number.
    -   If the business license contains a duplicate number, for example, \(1-1\), do not enter the duplicate number.
    -   Pay close attention to numbers and words with similar forms, such as the number 0 and the letter O, the number 1 and the letter I.
    -   Pay close attention to the number of digits of the certificate code. Enter the complete certificate number.

## Lack of identity documents of the domain holder {#section_itj_3rk_5gb .section}

If the system displays the message **Verification failed due to the lack of identity documents of the domain holder**, you can troubleshoot the fault as follows

-   If the domain name holder is a natural person, submit a scanned copy of the resident identity card or passport of the holder. For more information, see[Real-name authentication examples for individual domain holders](intl.en-US/Real-name authentication for domains /Real-name authentication examples/Real-name authentication examples for individual domain holders.md#).
-   If the domain name holder is an organization, submit a scanned copy of the business license, unified social credit code certificate, organization code certificate, or other valid certificates. For more information, see [Real-name authentication examples for organization domain holders](intl.en-US/Real-name authentication for domains /Real-name authentication examples/Real-name authentication examples for organization domain holders.md#).

## Incomplete information about the domain holder {#section_i5p_vrk_5gb .section}

If the system displays the message **Verification failed due to incomplete information about the domain holder**, you can troubleshoot the fault as follows

Submit a copy of the identity document or certificate. Include the borders of the document or certificate. If you use the business license, scan all information contained in the license, including any national emblem or seal affixed by the authority that manages the business license.

## Invalid holder information {#section_lxv_wrk_5gb .section}

If the system displays the message **Verification failed due to invalid holder information**, you can troubleshoot the fault as follows

Submit a copy of a valid identity document or certificate.

-   Mainland China holders
    -   We recommend that organization domain holders submit a scanned copy of a certificate that contains a valid **18-digit** unified social credit code, such as the business license, unified social credit code certificate, and organization code certificate.

    -   Natural persons can submit a copy of their resident identity card or residency certificate.

-   Non-mainland China holders
    -   Organization domain holders can submit a copy of other valid certificates.
    -   Natural persons can submit a copy of their passport or other valid identity documents.

## Failed attempts to upload the verification information to CNNIC {#section_mst_1sk_5gb .section}

If the system displays the message **Failed attempts to upload the verification information to CNNIC**, you can troubleshoot the fault as follows:

Check whether the format and size of the photo and the number of the certificate are correct.

-   Submit a scanned copy or photo of the certificate. The size of a scanned copy or photo must be from 55 KB to 1 MB. Supported photo formats include **JPG and BMP**.

    For other formats, use a graphics editor such as Microsoft Paint or Adobe Photoshop to convert them to the JPG or BMP format. **Do not change the file extension directly**.

-   You must submit a complete and clear scanned copy of the identity document with no cover or smudges. Include the borders of the identity document.
-   Use half-width characters when you enter the certificate number.

## Inconsistency between the submitted resident identity card and the one provided by the Ministry of Public Security {#section_aws_2sk_5gb .section}

If the system displays the message **Verification failed due to inconsistency between the submitted resident identity card and the one provided by the Ministry of Public Security**, you can troubleshoot the fault as follows

Check whether you have entered the correct holder name and the 18-digit resident identity card number.

**Note:** Individuals with special occupations, for example, military personnel and monks, cannot use the 18-digit resident identity card number for verification. We recommend that you use another identity document for the verification.

## International users {#section_swz_3sk_5gb .section}

If the system displays the message **Verification failed because the submitted information identifies the domain holder as an international user**, you can troubleshoot the fault as follows

International domain holders must keep the name of the domain holder consistent with that in the submitted verification information. If the verification information is written in English, enter the English name in the **Holder Name \(Chinese\)** field.

**Note:** CNNIC has not authorized the Alibaba Cloud China site to provide .cn, .中国, and .公司 domain name registration services to users other than mainland China, Hong Kong, and Macao organizations and individual users, and Taiwan individual users. Only mainland China, Hong Kong, and Macao organizations and individual users, and Taiwan individual users can complete the real-name authentication process for .cn, .中国, and .公司 domain names on the Alibaba Cloud China site. If you need to use a .cn domain name, register a .cn domain name and complete the real-name authentication process on the Alibaba Cloud International site. The process will be verified and regulated by CNNIC.

## Newly issued certificates or identity documents {#section_yyj_ksk_5gb .section}

If the system displays the message **Verification failed due to newly issued certificates or identity documents**, you can troubleshoot the fault as follows

The newly issued certificate or identity document has not been entered in the system of the verification authority. It takes at least 10 natural days to synchronize data. Submit the verification information 10 natural days after the certificate is issued.

## Incorrect contact information {#section_q1s_rgm_zgb .section}

If the system displays the message **Verification failed due to incorrect contact information. Command syntax errors occurred**, or **Verification failed due to incorrect contact information. XML schema validation failed**, you can troubleshoot the fault as follows

Check whether you have entered the correct country code in the domain registration information. For example, the country code for the People's Republic of China is 86. Do not enter the area code in the country code field. We recommend that you use the default code selected by the system.

## Sensitive words in domain names {#section_fh4_qdg_chb .section}

If the system displays the message **Verification failed due to content that may damage the honor and interests of the state**, or **Verification failed due to violation of China Internet Domain Name Regulations article 27: Those that insult or libel others and infringe other people's legal rights and interests** or **Other content prohibited by laws, rules and administrative regulations**, you can troubleshoot the fault as follows

We recommend that you use another domain name, or transfer your domain name to the Alibaba Cloud International site or other domain name service providers.

**Note:** Currently, the Alibaba Cloud International site only requires real-name authentication for .cn domain names.

## International individual or organization holders {#section_iqy_j5g_chb .section}

If the system displays the message **Verification failed due to international individual or organization holders**, you can troubleshoot the fault as follows

Check whether the region of the domain name holder is correct. Select the region specified in the submitted certificate or identity document. For example, if you are an individual domain holder and have submitted a scanned copy of a Mainland Travel Permit for Hong Kong and Macao Residents, select Hong Kong or Macao as specified by the permit.

