# Domain API 鉴权规则 {#concept_d3r_f2d_n2b .concept}

本文档介绍 Domain API 鉴权规则。

子账号通过 Domain API 访问主账号资源时需要遵循鉴权规则。

当子账号通过 Domain API 对主账号的 Domain 资源进行访问时，Domain 后台向 RAM 进行权限检查，以确保资源拥有者已向调用者授予了相关资源的相关权限。

根据涉及到的资源以及 API 的语义，每个 Domain API 会相应地确定需要检查哪些资源的权限。下表具体介绍了各 API 的鉴权规则：

|API|鉴权 Action|鉴权 Resource|
|:--|:--------|:----------|
|[SaveSingleTaskForUpdatingContactInfo](../../../../intl.zh-CN/API 参考/域名管理接口/提交域名信息修改任务.md#)|domain:DomainInfoModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForUpdatingContactInfo](../../../../intl.zh-CN/API 参考/域名管理接口/提交批量通过新联系人信息域名信息修改任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInReenterTransferAuthorizationCode](../../../../intl.zh-CN/API 参考/域名管理接口/域名转入重新输入转移密码.md#)|domain:DomainTransferInOperation|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInRefetchWhoisEmail](../../../../intl.zh-CN/API 参考/域名管理接口/域名转入重新抓取whois邮箱.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInResendMailToken](../../../../intl.zh-CN/API 参考/域名管理接口/域名转入重新发送验证邮件.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCancelingTransferIn](../../../../intl.zh-CN/API 参考/域名管理接口/提交取消域名转入任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCancelingTransferOut](../../../../intl.zh-CN/API 参考/域名管理接口/提交取消域名转出任务.md#)|domain:DomainTransferOutOperation|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForQueryingTransferAuthorizationCode](../../../../intl.zh-CN/API 参考/域名管理接口/提交获取域名转移密码任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForModifyingDnsHost](../../../../intl.zh-CN/API 参考/域名管理接口/提交修改dnshost任务.md#)|domain:DnsHostModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCreatingDnsHost](../../../../intl.zh-CN/API 参考/域名管理接口/提交创建dnshost任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForSynchronizingDnsHost](../../../../intl.zh-CN/API 参考/域名管理接口/提交同步dnshost任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForDeletingDnsHost|acs:domain:\*:$accountid:domain/$domainName|
|[SaveBatchTaskForModifyingDomainDns](../../../../intl.zh-CN/API 参考/域名管理接口/提交批量修改域名DNS任务.md#)|domain:DnsModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForTransferProhibitionLock](../../../../intl.zh-CN/API 参考/域名管理接口/提交禁止转移锁任务.md#)|domain:SecuritySetting|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForTransferProhibitionLock](../../../../intl.zh-CN/API 参考/域名管理接口/提交批量禁止转移锁任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForUpdateProhibitionLock](../../../../intl.zh-CN/API 参考/域名管理接口/提交禁止更新锁任务.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForUpdateProhibitionLock](../../../../intl.zh-CN/API 参考/域名管理接口/提交批量禁止更新锁任务.md#)|acs:domain:\*:$accountid:domain/$domainName|

|API|鉴权 Action|鉴权 Resource|
|:--|:--------|:----------|
|[QueryDomainList](../../../../intl.zh-CN/API 参考/域名管理接口/查询域名列表.md#)|domain:QueryCommonInfo|acs:domain:\*:$accountid:\* |
|[QueryDomainByInstanceId](../../../../intl.zh-CN/API 参考/域名管理接口/查询域名信息.md#)|acs:domain:\*:$accountid:\* |
|[QueryContactInfo](../../../../intl.zh-CN/API 参考/域名管理接口/查询联系人信息.md#)|acs:domain:\*:$accountid:\* |
|[VerifyContactField](../../../../intl.zh-CN/API 参考/域名管理接口/校验联系人信息.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskList](../../../../intl.zh-CN/API 参考/域名管理接口/查询任务列表.md#)|domain:QueryDomainTask|acs:domain:\*:$accountid:\* |
|[QueryTaskInfoHistory](../../../../intl.zh-CN/API 参考/域名管理接口/查询任务历史列表.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskDetailList](../../../../intl.zh-CN/API 参考/域名管理接口/查询任务详情.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskDetailHistory](../../../../intl.zh-CN/API 参考/域名管理接口/查询任务历史详情.md#)|acs:domain:\*:$accountid:\* |
|[PollTaskResult](../../../../intl.zh-CN/API 参考/域名管理接口/查询已经执行完成的任务详情列表.md#)|acs:domain:\*:$accountid:\* |
|[QueryChangeLogList](../../../../intl.zh-CN/API 参考/域名管理接口/查询操作日志.md#)|domain:QueryChangeLog|acs:domain:\*:$accountid:\* |
|[QueryTransferInByInstanceId](../../../../intl.zh-CN/API 参考/域名管理接口/根据实例编号查询域名转入信息.md#)|domain:QueryDomainTransferIn|acs:domain:\*:$accountid:\* |
|[QueryTransferInList](../../../../intl.zh-CN/API 参考/域名管理接口/查询域名转入列表.md#)|acs:domain:\*:$accountid:\* |
|[CheckTransferInFeasibility](../../../../intl.zh-CN/API 参考/域名管理接口/校验域名是否可以转入.md#)|acs:domain:\*:$accountid:\* |
|[TransferInCheckMailToken](../../../../intl.zh-CN/API 参考/域名管理接口/域名转入验证邮件.md#)|domain:TransferInCheckMailToken|acs:domain:\*:$accountid:\* |
|[QueryTransferOutInfo](../../../../intl.zh-CN/API 参考/域名管理接口/查询域名转出信息.md#)|domain:QueryDomainTransferOut|acs:domain:\*:$accountid:\* |
|[QueryDnsHost](../../../../intl.zh-CN/API 参考/域名管理接口/查询域名DnsHost.md#)|domain:QueryDnsHost|acs:domain:\*:$accountid:\* |
|[QueryRegistrantProfiles](../../../../intl.zh-CN/API 参考/信息模板接口/查询信息模板.md#)|domain:QueryRegistrantProfile|acs:domain:\*:$accountid:\* |
|[ListEmailVerification](../../../../intl.zh-CN/API 参考/域名管理接口/查询邮箱验证列表.md#)|domain:QueryEmailVerification|acs:domain:\*:$accountid:\* |
|[AcknowledgeTaskResult](../../../../intl.zh-CN/API 参考/域名管理接口/确认任务详情结果.md#)|domain:AcknowledgeTaskResult|acs:domain:\*:$accountid:\* |
|[SaveRegistrantProfile](../../../../intl.zh-CN/API 参考/信息模板接口/保存信息模板.md#)|domain:RegistrantProfileOperation|acs:domain:\*:$accountid:\* |
|[DeleteRegistrantProfile](../../../../intl.zh-CN/API 参考/信息模板接口/删除信息模板.md#)|acs:domain:\*:$accountid:\* |
|[DeleteEmailVerification](../../../../intl.zh-CN/API 参考/域名管理接口/删除邮箱验证.md#)|domain:EmailVerificationOperation|acs:domain:\*:$accountid:\* |
|[VerifyEmail](../../../../intl.zh-CN/API 参考/域名管理接口/验证邮箱Token.md#)|acs:domain:\*:$accountid:\* |
|[ResendEmailVerification](../../../../intl.zh-CN/API 参考/域名管理接口/重新发送验证邮件.md#)|acs:domain:\*:$accountid:\* |
|[SubmitEmailVerification](../../../../intl.zh-CN/API 参考/域名管理接口/发送邮件验证邮件.md#)|acs:domain:\*:$accountid:\* |

|API|鉴权 Action|鉴权 Resource|
|:--|:--------|:----------|
|\*|domain:\*|acs:domain:\*:$accountid:\*|

