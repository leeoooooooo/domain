# 自定义DNS服务器 FAQ {#concept_gp2_2sd_b2b .concept}

-   [什么是自定义 DNS 服务器？](#section_rbt_xsd_b2b)
-   [服务器名称如何填写？](#section_sbt_xsd_b2b)
-   [最多支持多少个 DNS 服务器创建？](#section_tbt_xsd_b2b)
-   [支持 IPv6 吗？](#section_ubt_xsd_b2b)
-   [最多支持多少个 IP 地址？](#section_vbt_xsd_b2b)
-   [服务器名称可以修改或删除吗？](#section_wbt_xsd_b2b)
-   [IP 地址可以修改或删除吗？](#section_xbt_xsd_b2b)
-   [创建 DNS 服务器成功后，还需要做什么操作？](#section_ybt_xsd_b2b)
-   [创建服务器成功后，就会立即生效吗？](#section_act_xsd_b2b)

## 什么是自定义 DNS 服务器？ {#section_rbt_xsd_b2b .section}

自定义 DNS，是指使用当前的域名创建自己的 DNS 服务器，由自己创建的 DNS 服务器提供解析服务。创建 DNS 需要用户具备专业技术基础，否则不建议自己创建，直接使用域名服务商提供的 DNS 解析服务即可。

## 服务器名称如何填写？ {#section_sbt_xsd_b2b .section}

DNS 服务器名称合法格式：只能包括英文字母（a-z，不区分大小写）、数字（0-9）、点号（.）以及连字符 \(-\)，且点号和连字符不能在开头和结尾位置；不能使用空格及特殊字符\(如 !、$、&、? 等\)；允许最长字符为 80 个。

一般建议使用 dns 或 ns 作为服务器名称。如：dns1.yourdomain.com/ dns2.yourdomain.com。

## 最多支持多少个 DNS 服务器创建？ {#section_tbt_xsd_b2b .section}

最多支持 13 个，具体以对应注册局规则为准。

## 支持 IPv6 吗？ {#section_ubt_xsd_b2b .section}

支持。

## 最多支持多少个 IP 地址？ {#section_vbt_xsd_b2b .section}

DNS 服务器对应的 IP 地址，最少填写 1 个，最多填写 13 个。具体以对应注册局规则为准。

## 服务器名称可以修改或删除吗？ {#section_wbt_xsd_b2b .section}

不支持。

## IP 地址可以修改或删除吗？ {#section_xbt_xsd_b2b .section}

IP 地址可以修改或删除，但最少要保留一个 IP 地址。

## 创建 DNS 服务器成功后，还需要做什么操作？ {#section_ybt_xsd_b2b .section}

用户还需要在当前域名 DNS 上添加对应 A 记录，用户已创建 DNS 服务器才会最终生效。

举例如下：用户域名 a.com，要创建 ns1.a.com DNS 服务器（如：IP 地址为 1.1.1.1）。

-   如果域名 a.com 使用的是阿里云云解析 DNS：

    ns1.hichina.com/ns2.ahichina.com； 用户在创建 ns1.a.com 服务器之前或之后，还需要在阿里云云解析 DNS 增加一条 ns1.a.com 的 A 记录，指向所创建的 IP 地址（如 1.1.1.1）。

-   如果所创建的 DNS 服务器 ns1.a.com 用来解析当前域名 a.com，请务必在 ns1.a.com 对应服务器上增加一个 A 记录（如：IP 地址为 1.1.1.1）。


## 创建服务器成功后，就会立即生效吗？ {#section_act_xsd_b2b .section}

一般创建完成后，几分钟即可生效。

