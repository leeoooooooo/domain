# 可授权 Domain 资源类型 {#concept_r2k_lhc_n2b .concept}

本文档介绍可授权 Domain 资源类型。

目前，可以在 RAM 中进行授权的资源类型及描述方式如下表所示：

|资源类型|授权策略中的资源描述方式|描述方式|
|:---|:-----------|:---|
|Domain| acs:domain:\*:$accountid:\*

 acs:domain:\*:$accountid:domain/$domainName

 |授权子账户管理自己的域名，例如域名信息修改（过户）、实名认证、DNS设置、安全设置、域名转入转出等。|

