# API概览 {#concept_xt1_n2b_b2b .concept}

支持域名购买、续费以及管理操作（包括信息修改、DNS修改、创建DNS、信息模板的管理等），以及域名列表和域名信息的查询。

## 域名管理接口 {#section_z25_r2b_b2b .section}

|API|描述|
|:--|:-|
|[QueryDomainList](intl.zh-CN/API 参考/域名管理接口/查询域名列表.md#)|查询自己账户下域名列表|
|[QueryDomainByInstanceId](intl.zh-CN/API 参考/域名管理接口/查询域名信息.md#)|查询自己账户下域名信息|
|[QueryContactInfo](intl.zh-CN/API 参考/域名管理接口/查询联系人信息.md#)|查询域名联系人信息|
|[QueryChangeLogList](intl.zh-CN/API 参考/域名管理接口/查询操作日志.md#)|查询操作日志|
|[DeleteEmailVerification](intl.zh-CN/API 参考/域名管理接口/删除邮箱验证.md#)|删除邮箱验证|
|[VerifyEmail](intl.zh-CN/API 参考/域名管理接口/验证邮箱Token.md#)|验证邮箱|
|[ListEmailVerification](intl.zh-CN/API 参考/域名管理接口/查询邮箱验证列表.md#)|查询邮箱验证列表|
|[ResendEmailVerification](intl.zh-CN/API 参考/域名管理接口/重新发送验证邮件.md#)|重新发送验证邮件|
|[SubmitEmailVerification](intl.zh-CN/API 参考/域名管理接口/发送邮件验证邮件.md#)|发送邮箱验证列表|
|[SaveSingleTaskForCreatingOrderActivate](intl.zh-CN/API 参考/域名管理接口/提交域名注册任务.md#)|提交域名注册任务|
|[SaveSingleTaskForCreatingOrderRenew](intl.zh-CN/API 参考/域名管理接口/提交域名续费任务.md#)|提交域名续费任务|
|[SaveBatchTaskForModifyingDomainDns](intl.zh-CN/API 参考/域名管理接口/提交批量修改域名DNS任务.md#)|提交批量修改域名dns任务|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](intl.zh-CN/API 参考/域名管理接口/提交批量通过新联系人信息域名信息修改任务.md#)|提交批量通过联系人信息和资料修改注册联系人信息任务|
|[SaveBatchTaskForCreatingOrderActivate](intl.zh-CN/API 参考/域名管理接口/提交批量域名注册任务.md#)|提交批量域名注册任务|
|[SaveBatchTaskForCreatingOrderRenew](intl.zh-CN/API 参考/域名管理接口/提交批量域名续费任务.md#)|提交批量域名续费任务|
|[SaveBatchTaskForUpdateProhibitionLock](intl.zh-CN/API 参考/域名管理接口/提交批量禁止更新锁任务.md#)|提交批量禁止更新锁任务|
|[SaveBatchTaskForTransferProhibitionLock](intl.zh-CN/API 参考/域名管理接口/提交批量禁止转移锁任务.md#)|提交批量禁止转移锁任务|
|[QueryTaskList](intl.zh-CN/API 参考/域名管理接口/查询任务列表.md#)|查询域名任务列表|
|[QueryTaskInfoHistory](intl.zh-CN/API 参考/域名管理接口/查询任务历史列表.md#)|查询域名任务历史列表|
|[QueryTaskDetailList](intl.zh-CN/API 参考/域名管理接口/查询任务详情.md#)|查询域名任务的详情列表|
|[QueryTaskDetailHistory](intl.zh-CN/API 参考/域名管理接口/查询任务历史详情.md#)|查询域名任务的详情历史列表|
|[CheckDomain](intl.zh-CN/API 参考/域名管理接口/检查域名是否可以注册.md#)|检查域名是否可以注册接口|
|[FuzzyMatchDomainSensitiveWord](intl.zh-CN/API 参考/域名管理接口/检查是否包含敏感词.md#)|检查是否包含敏感词|
|[BatchFuzzyMatchDomainSensitiveWord](intl.zh-CN/API 参考/域名管理接口/批量检查是否包含敏感词.md#)|批量检查是否包含敏感词|
|[CheckDomainSunriseClaim](intl.zh-CN/API 参考/域名管理接口/查询商标词key.md#)|查询商标词key|
|[LookupTmchNotice](intl.zh-CN/API 参考/域名管理接口/域名查询商标词tmch信息.md#)|查询tmch信息|
|[AcknowledgeTaskResult](intl.zh-CN/API 参考/域名管理接口/确认任务详情结果.md#)|确认任务详情结果|
|[CheckTransferInFeasibility](intl.zh-CN/API 参考/域名管理接口/校验域名是否可以转入.md#)|校验域名是否可以转入|
|[PollTaskResult](intl.zh-CN/API 参考/域名管理接口/查询已经执行完成的任务详情列表.md#)|查询已经执行完成的任务详情列表|
|[QueryTransferInByInstanceId](intl.zh-CN/API 参考/域名管理接口/根据实例编号查询域名转入信息.md#)|根据实例编号查询域名转入信息|
|[QueryTransferInList](intl.zh-CN/API 参考/域名管理接口/查询域名转入列表.md#)|查询域名转入列表|
|[QueryTransferOutInfo](intl.zh-CN/API 参考/域名管理接口/查询域名转出信息.md#)|查询域名转出信息|
|[QueryDomainAdminDivision](intl.zh-CN/API 参考/域名管理接口/查询中国行政区划.md#)|查询中国行政区划|
|[SaveSingleTaskForCancelingTransferIn](intl.zh-CN/API 参考/域名管理接口/提交取消域名转入任务.md#)|提交取消域名转入任务|
|[SaveSingleTaskForCancelingTransferOut](intl.zh-CN/API 参考/域名管理接口/提交取消域名转出任务.md#)|提交取消域名转出任务|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](intl.zh-CN/API 参考/域名管理接口/提交获取域名转移密码任务.md#)|提交获取域名转移密码任务|
|[TransferInCheckMailToken](intl.zh-CN/API 参考/域名管理接口/域名转入验证邮件.md#)|域名转入验证邮件|
|[TransferInReenterTransferAuthorizationCode](intl.zh-CN/API 参考/域名管理接口/域名转入重新输入转移密码.md#)|域名转入重新输入转移密码|
|[TransferInRefetchWhoisEmail](intl.zh-CN/API 参考/域名管理接口/域名转入重新抓取whois邮箱.md#)|域名转入重新抓取whois邮箱|
|[TransferInResendMailToken](intl.zh-CN/API 参考/域名管理接口/域名转入重新发送验证邮件.md#)|域名转入重新发送验证邮件|
|[VerifyContactField](intl.zh-CN/API 参考/域名管理接口/校验联系人信息.md#)|校验联系人信息|
|[SaveSingleTaskForCreatingOrderRedeem](intl.zh-CN/API 参考/域名管理接口/提交域名赎回任务.md#)|提交域名赎回任务|
|[SaveBatchTaskForCreatingOrderRedeem](intl.zh-CN/API 参考/域名管理接口/提交批量域名赎回任务.md#)|提交批量域名赎回任务|
|[SaveSingleTaskForCreatingDnsHost](intl.zh-CN/API 参考/域名管理接口/提交创建dnshost任务.md#)|提交创建dnshost任务|
|[SaveSingleTaskForModifyingDnsHost](intl.zh-CN/API 参考/域名管理接口/提交修改dnshost任务.md#)|提交修改dnshost任务|
|[SaveSingleTaskForSynchronizingDnsHost](intl.zh-CN/API 参考/域名管理接口/提交同步dnshost任务.md#)|提交同步dnshost任务|
|[SaveSingleTaskForTransferProhibitionLock](intl.zh-CN/API 参考/域名管理接口/提交禁止转移锁任务.md#)|提交禁止转移锁任务|
|[SaveSingleTaskForUpdateProhibitionLock](intl.zh-CN/API 参考/域名管理接口/提交禁止更新锁任务.md#)|提交禁止更新锁任务|
|[SaveSingleTaskForUpdatingContactInfo](intl.zh-CN/API 参考/域名管理接口/提交域名信息修改任务.md#)|提交域名域名信息修改任务|
|[QueryDnsHost](intl.zh-CN/API 参考/域名管理接口/查询域名DnsHost.md#)|查询域名dnshost|
|[SaveBatchDomainRemark](intl.zh-CN/API 参考/域名管理接口/批量保存域名备注.md#)|批量保存域名备注信息|
|[QueryDomainSuffix](intl.zh-CN/API 参考/域名管理接口/高级搜索后缀列表.md#)|高级搜索自己账户下后缀列表|
|[QueryAdvancedDomainList](intl.zh-CN/API 参考/域名管理接口/高级搜索域名列表.md#)|高级搜索自己账号下域名列表|

## 信息模板接口 {#section_zdt_d3b_b2b .section}

|API|描述|
|:--|:-|
|[SaveRegistrantProfile](intl.zh-CN/API 参考/信息模板接口/保存信息模板.md#)|创建或者保存域名信息模板|
|[QueryRegistrantProfiles](intl.zh-CN/API 参考/信息模板接口/查询信息模板.md#)|查询自己账户下的域名信息模板|
|[DeleteRegistrantProfile](intl.zh-CN/API 参考/信息模板接口/删除信息模板.md#)|删除指定的域名信息模板|

