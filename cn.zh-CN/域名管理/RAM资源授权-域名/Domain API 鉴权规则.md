# Domain API 鉴权规则 {#concept_d3r_f2d_n2b .concept}

本文档介绍 Domain API 鉴权规则。

子账号通过 Domain API 访问主账号资源时需要遵循鉴权规则。

当子账号通过 Domain API 对主账号的 Domain 资源进行访问时，Domain 后台向 RAM 进行权限检查，以确保资源拥有者已向调用者授予了相关资源的相关权限。

根据涉及到的资源以及 API 的语义，每个 Domain API 会相应地确定需要检查哪些资源的权限。下表具体介绍了各 API 的鉴权规则：

|API|鉴权 Action|鉴权 Resource|
|:--|:--------|:----------|
|[SaveSingleTaskForUpdatingContactInfo](../../../../../cn.zh-CN/API 参考/域名管理接口/提交域名信息修改任务.md#)|domain:DomainInfoModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForUpdatingContactInfoByNewContact](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量通过新联系人信息域名信息修改任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量通过模板域名信息修改任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID](../../../../../cn.zh-CN/API 参考/域名管理接口/提交通过信息模板ID提交修改注册联系人信息任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveTaskForUpdatingRegistrantInfoByIdentityCredential](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量通过联系人信息和资料修改注册联系人信息任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileID](../../../../../cn.zh-CN/API 参考/域名管理接口/通过信息模板ID提交域名实名认证任务.md#)|domain:RealNameVerificationOperation|acs:domain:\*:$accountid:domain/$domainName |
|CancelDomainVerification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveTaskForSubmittingDomainRealNameVerificationByIdentityCredential](../../../../../cn.zh-CN/API 参考/域名管理接口/提交域名实名认证任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInReenterTransferAuthorizationCode](../../../../../cn.zh-CN/API 参考/域名管理接口/域名转入重新输入转移密码.md#)|domain:DomainTransferInOperation|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInRefetchWhoisEmail](../../../../../cn.zh-CN/API 参考/域名管理接口/域名转入重新抓取whois邮箱.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInResendMailToken](../../../../../cn.zh-CN/API 参考/域名管理接口/域名转入重新发送验证邮件.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCancelingTransferIn](../../../../../cn.zh-CN/API 参考/域名管理接口/提交取消域名转入任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCancelingTransferOut](../../../../../cn.zh-CN/API 参考/域名管理接口/提交取消域名转出任务.md#)|domain:DomainTransferOutOperation|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForQueryingTransferAuthorizationCode](../../../../../cn.zh-CN/API 参考/域名管理接口/提交获取域名转移密码任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForModifyingDnsHost](../../../../../cn.zh-CN/API 参考/域名管理接口/提交修改dnshost任务.md#)|domain:DnsHostModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCreatingDnsHost](../../../../../cn.zh-CN/API 参考/域名管理接口/提交创建dnshost任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForSynchronizingDnsHost](../../../../../cn.zh-CN/API 参考/域名管理接口/提交同步dnshost任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForDeletingDnsHost|acs:domain:\*:$accountid:domain/$domainName|
|[SaveBatchTaskForModifyingDomainDns](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量修改域名DNS任务.md#)|domain:DnsModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForTransferProhibitionLock](../../../../../cn.zh-CN/API 参考/域名管理接口/提交禁止转移锁任务.md#)|domain:SecuritySetting|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForTransferProhibitionLock](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量禁止转移锁任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForUpdateProhibitionLock](../../../../../cn.zh-CN/API 参考/域名管理接口/提交禁止更新锁任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForUpdateProhibitionLock](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量禁止更新锁任务.md#)|acs:domain:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForCreatingOrderRenew](../../../../../cn.zh-CN/API 参考/域名管理接口/提交域名续费任务.md#)|domain:CreateOrderRenew|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForCreatingOrderRenew](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量域名续费任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCreatingOrderRedeem](../../../../../cn.zh-CN/API 参考/域名管理接口/提交域名赎回任务.md#)|domain:CreateOrderRedeem|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForCreatingOrderRedeem](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量域名赎回任务.md#)|acs:domain:\*:$accountid:domain/$domainName |

|API|鉴权 Action|鉴权 Resource|
|:--|:--------|:----------|
|[QueryDomainList](../../../../../cn.zh-CN/API 参考/域名管理接口/查询域名列表.md#)|domain:QueryCommonInfo|acs:domain:\*:$accountid:\* |
|[QueryDomainByInstanceId](../../../../../cn.zh-CN/API 参考/域名管理接口/查询域名信息.md#)|acs:domain:\*:$accountid:\* |
|[QueryContactInfo](../../../../../cn.zh-CN/API 参考/域名管理接口/查询联系人信息.md#)|acs:domain:\*:$accountid:\* |
|[QueryDomainSuffix](../../../../../cn.zh-CN/API 参考/域名管理接口/高级搜索后缀列表.md#)|acs:domain:\*:$accountid:\* |
|[QueryAdvancedDomainList](../../../../../cn.zh-CN/API 参考/域名管理接口/高级搜索域名列表.md#)|acs:domain:\*:$accountid:\* |
|[VerifyContactField](../../../../../cn.zh-CN/API 参考/域名管理接口/校验联系人信息.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskList](../../../../../cn.zh-CN/API 参考/域名管理接口/查询任务列表.md#)|domain:QueryDomainTask|acs:domain:\*:$accountid:\* |
|[QueryTaskInfoHistory](../../../../../cn.zh-CN/API 参考/域名管理接口/查询任务历史列表.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskDetailList](../../../../../cn.zh-CN/API 参考/域名管理接口/查询任务详情.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskDetailHistory](../../../../../cn.zh-CN/API 参考/域名管理接口/查询任务历史详情.md#)|acs:domain:\*:$accountid:\* |
|[PollTaskResult](../../../../../cn.zh-CN/API 参考/域名管理接口/查询已经执行完成的任务详情列表.md#)|acs:domain:\*:$accountid:\* |
|[QueryChangeLogList](../../../../../cn.zh-CN/API 参考/域名管理接口/查询操作日志.md#)|domain:QueryChangeLog|acs:domain:\*:$accountid:\* |
|[QueryTransferInByInstanceId](../../../../../cn.zh-CN/API 参考/域名管理接口/根据实例编号查询域名转入信息.md#)|domain:QueryDomainTransferIn|acs:domain:\*:$accountid:\* |
|[QueryTransferInList](../../../../../cn.zh-CN/API 参考/域名管理接口/查询域名转入列表.md#)|acs:domain:\*:$accountid:\* |
|[CheckTransferInFeasibility](../../../../../cn.zh-CN/API 参考/域名管理接口/校验域名是否可以转入.md#)|acs:domain:\*:$accountid:\* |
|[TransferInCheckMailToken](../../../../../cn.zh-CN/API 参考/域名管理接口/域名转入验证邮件.md#)|domain:TransferInCheckMailToken|acs:domain:\*:$accountid:\* |
|[QueryTransferOutInfo](../../../../../cn.zh-CN/API 参考/域名管理接口/查询域名转出信息.md#)|domain:QueryDomainTransferOut|acs:domain:\*:$accountid:\* |
|[QueryDnsHost](../../../../../cn.zh-CN/API 参考/域名管理接口/查询域名DnsHost.md#)|domain:QueryDnsHost|acs:domain:\*:$accountid:\* |
|[QueryFailReasonForRegistrantProfileRealNameVerification](../../../../../cn.zh-CN/API 参考/信息模板接口/查询模板实名认证失败原因.md#)|domain:QueryRegistrantProfile|acs:domain:\*:$accountid:\* |
|[QueryRegistrantProfileRealNameVerificationInfo](../../../../../cn.zh-CN/API 参考/信息模板接口/查询信息模板实名认证资料.md#)|acs:domain:\*:$accountid:\* |
|[QueryRegistrantProfiles](../../../../../cn.zh-CN/API 参考/信息模板接口/查询信息模板实名认证资料.md#)|acs:domain:\*:$accountid:\* |
|QueryDomainGroupList|domain:QueryDomainGroup|acs:domain:\*:$accountid:\* |
|[QueryFailReasonForDomainRealNameVerification](../../../../../cn.zh-CN/API 参考/域名管理接口/查询域名实名认证失败原因.md#)|domain:QueryRealNameVerification|acs:domain:\*:$accountid:\* |
|QueryDomainRealNameVerificationInfo|acs:domain:\*:$accountid:\* |
|[ListEmailVerification](../../../../../cn.zh-CN/API 参考/域名管理接口/查询邮箱验证列表.md#)|domain:QueryEmailVerification|acs:domain:\*:$accountid:\* |
|QueryEmailVerification|acs:domain:\*:$accountid:\* |
|[AcknowledgeTaskResult](../../../../../cn.zh-CN/API 参考/域名管理接口/确认任务详情结果.md#)|domain:AcknowledgeTaskResult|acs:domain:\*:$accountid:\* |
|[SaveRegistrantProfile](../../../../../cn.zh-CN/API 参考/信息模板接口/保存信息模板.md#)|domain:RegistrantProfileOperation|acs:domain:\*:$accountid:\* |
|[DeleteRegistrantProfile](../../../../../cn.zh-CN/API 参考/信息模板接口/删除信息模板.md#)|acs:domain:\*:$accountid:\* |
|[RegistrantProfileRealNameVerification](../../../../../cn.zh-CN/API 参考/信息模板接口/提交信息模板实名认证.md#)|acs:domain:\*:$accountid:\* |
|[DeleteDomainGroup](../../../../../cn.zh-CN/API 参考/域名管理接口/删除域名分组.md#)|domain:DomainGroupOperation|acs:domain:\*:$accountid:\* |
|[SaveDomainGroup](../../../../../cn.zh-CN/API 参考/域名管理接口/保存域名分组.md#)|acs:domain:\*:$accountid:\* |
|[UpdateDomainToDomainGroup](../../../../../cn.zh-CN/API 参考/域名管理接口/向分组中设置域名.md#)|acs:domain:\*:$accountid:\* |
|[DeleteEmailVerification](../../../../../cn.zh-CN/API 参考/域名管理接口/删除邮箱验证.md#)|domain:EmailVerificationOperation|acs:domain:\*:$accountid:\* |
|[VerifyEmail](../../../../../cn.zh-CN/API 参考/域名管理接口/验证邮箱Token.md#)|acs:domain:\*:$accountid:\* |
|[ResendEmailVerification](../../../../../cn.zh-CN/API 参考/域名管理接口/重新发送验证邮件.md#)|acs:domain:\*:$accountid:\* |
|[SubmitEmailVerification](../../../../../cn.zh-CN/API 参考/域名管理接口/发送邮件验证邮件.md#)|acs:domain:\*:$accountid:\* |
|[SaveBatchDomainRemark](../../../../../cn.zh-CN/API 参考/域名管理接口/批量保存域名备注.md#)|domain:DomainInfoModification|acs:domain:\*:$accountid:\* |
|[SaveSingleTaskForCreatingOrderActivate](../../../../../cn.zh-CN/API 参考/域名管理接口/提交域名注册任务.md#)|domain:CreateOrderActivate|acs:domain:\*:$accountid:\* |
|[SaveBatchTaskForCreatingOrderActivate](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量域名注册任务.md#)|acs:domain:\*:$accountid:\* |
|[SaveSingleTaskForCreatingOrderTransfer](../../../../../cn.zh-CN/API 参考/域名管理接口/提交域名转入任务.md#)|domain:CreateOrderTransfer|acs:domain:\*:$accountid:\* |
|[SaveBatchTaskForCreatingOrderTransfer](../../../../../cn.zh-CN/API 参考/域名管理接口/提交批量域名转入任务.md#)|acs:domain:\*:$accountid:\* |

|API|鉴权 Action|鉴权 Resource|
|:--|:--------|:----------|
|\*|domain:\*|acs:domain:\*:$accountid:\*|

