# Domain API Authentication Rules {#concept_d3r_f2d_n2b .concept}

This document describes domain API authentication rules.

DNS API authentication rules for access to the main account resources by sub-accounts.

When a RAM user requests access to the Domain resources of the primary account by using the Domain APIs, the Domain backend sends a request to RAM to perform the request authentication. This authentication ensures that the resource owner indeed has granted access to these resources to the caller.

For each Domain API, the resources need to be checked are determined by the involved resources and the semantics of the API. The following table lists the authentication rules for each API.

|API|Authorization action|Authorization Resource|
|:--|:-------------------|:---------------------|
|[SaveSingleTaskForUpdatingContactInfo](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdatingContactInfo.md#)|domain:DomainInfoModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForUpdatingContactInfo](../../../../../intl.en-US/API Reference (New)/Domain management/Submit a batch task for modifying domain name information by new registrant.md#)|acs:domain:\*:$accountid:domain/$domainName |
|SaveBatchTaskForUpdatingContactInfoByNewContact|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInReenterTransferAuthorizationCode](../../../../../intl.en-US/API Reference (New)/Domain management/TransferInReenterTransferAuthorizationCode.md#)|domain:DomainTransferInOperation|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInRefetchWhoisEmail](../../../../../intl.en-US/API Reference (New)/Domain management/TransferInRefetchWhoisEmail.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[TransferInResendMailToken](../../../../../intl.en-US/API Reference (New)/Domain management/TransferInResendMailToken.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCancelingTransferIn](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferIn.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCancelingTransferOut](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferOut.md#)|domain:DomainTransferOutOperation|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForQueryingTransferAuthorizationCode](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForQueryingTransferAuthorizationCode.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForModifyingDnsHost](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForModifyingDnsHost.md#)|domain:DnsHostModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForCreatingDnsHost](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingDnsHost.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForSynchronizingDnsHost](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForSynchronizingDnsHost.md#)|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForDeletingDnsHost|acs:domain:\*:$accountid:domain/$domainName|
|[SaveBatchTaskForModifyingDomainDns](../../../../../intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForModifyingDomainDns.md#)|domain:DnsModification|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForTransferProhibitionLock](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForTransferProhibitionLock.md#)|domain:SecuritySetting|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForTransferProhibitionLock](../../../../../intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForTransferProhibitionLock.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveSingleTaskForUpdateProhibitionLock](../../../../../intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdateProhibitionLock.md#)|acs:domain:\*:$accountid:domain/$domainName |
|[SaveBatchTaskForUpdateProhibitionLock](../../../../../intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForUpdateProhibitionLock.md#)|acs:domain:\*:$accountid:domain/$domainName|

|API|Authorization action|Authorization Resource|
|:--|:-------------------|:---------------------|
|[QueryDomainList](../../../../../intl.en-US/API Reference (New)/Domain management/QueryDomainList.md#)|domain:QueryCommonInfo|acs:domain:\*:$accountid:\* |
|[QueryDomainByInstanceId](../../../../../intl.en-US/API Reference (New)/Domain management/QueryDomainByInstanceId.md#)|acs:domain:\*:$accountid:\* |
|[QueryContactInfo](../../../../../intl.en-US/API Reference (New)/Domain management/QueryContactInfo.md#)|acs:domain:\*:$accountid:\* |
|[VerifyContactField](../../../../../intl.en-US/API Reference (New)/Domain management/VerifyContactField.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskList](../../../../../intl.en-US/API Reference (New)/Domain management/QueryTaskList.md#)|domain:QueryDomainTask|acs:domain:\*:$accountid:\* |
|[QueryTaskInfoHistory](../../../../../intl.en-US/API Reference (New)/Domain management/QueryTaskInfoHistory.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskDetailList](../../../../../intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#)|acs:domain:\*:$accountid:\* |
|[QueryTaskDetailHistory](../../../../../intl.en-US/API Reference (New)/Domain management/QueryTaskDetailHistory.md#)|acs:domain:\*:$accountid:\* |
|[PollTaskResult](../../../../../intl.en-US/API Reference (New)/Domain management/PollTaskResult.md#)|acs:domain:\*:$accountid:\* |
|[QueryChangeLogList](../../../../../intl.en-US/API Reference (New)/Domain management/QueryChangeLogList.md#)|domain:QueryChangeLog|acs:domain:\*:$accountid:\* |
|[QueryTransferInByInstanceId](../../../../../intl.en-US/API Reference (New)/Domain management/QueryTransferInByInstanceId.md#)|domain:QueryDomainTransferIn|acs:domain:\*:$accountid:\* |
|[QueryTransferInList](../../../../../intl.en-US/API Reference (New)/Domain management/QueryTransferInList.md#)|acs:domain:\*:$accountid:\* |
|[CheckTransferInFeasibility](../../../../../intl.en-US/API Reference (New)/Domain management/CheckTransferInFeasibility.md#)|acs:domain:\*:$accountid:\* |
|[TransferInCheckMailToken](../../../../../intl.en-US/API Reference (New)/Domain management/TransferInCheckMailToken.md#)|domain:TransferInCheckMailToken|acs:domain:\*:$accountid:\* |
|[QueryTransferOutInfo](../../../../../intl.en-US/API Reference (New)/Domain management/QueryTransferOutInfo.md#)|domain:QueryDomainTransferOut|acs:domain:\*:$accountid:\* |
|[QueryDnsHost](../../../../../intl.en-US/API Reference (New)/Domain management/QueryDnsHost.md#)|domain:QueryDnsHost|acs:domain:\*:$accountid:\* |
|[QueryRegistrantProfiles](../../../../../intl.en-US/API Reference (New)/Information template/QueryRegistrantProfiles.md#)|domain:QueryRegistrantProfile|acs:domain:\*:$accountid:\* |
|[ListEmailVerification](../../../../../intl.en-US/API Reference (New)/Domain management/ListEmailVerification.md#)|domain:QueryEmailVerification|acs:domain:\*:$accountid:\* |
|[AcknowledgeTaskResult](../../../../../intl.en-US/API Reference (New)/Domain management/AcknowledgeTaskResult.md#)|domain:AcknowledgeTaskResult|acs:domain:\*:$accountid:\* |
|[SaveRegistrantProfile](../../../../../intl.en-US/API Reference (New)/Information template/SaveRegistrantProfile.md#)|domain:RegistrantProfileOperation|acs:domain:\*:$accountid:\* |
|[DeleteRegistrantProfile](../../../../../intl.en-US/API Reference (New)/Information template/DeleteRegistrantProfile.md#)|acs:domain:\*:$accountid:\* |
|[DeleteEmailVerification](../../../../../intl.en-US/API Reference (New)/Domain management/DeleteEmailVerification.md#)|domain:EmailVerificationOperation|acs:domain:\*:$accountid:\* |
|[VerifyEmail](../../../../../intl.en-US/API Reference (New)/Domain management/VerifyEmail.md#)|acs:domain:\*:$accountid:\* |
|[ResendEmailVerification](../../../../../intl.en-US/API Reference (New)/Domain management/ResendEmailVerification.md#)|acs:domain:\*:$accountid:\* |
|[SubmitEmailVerification](../../../../../intl.en-US/API Reference (New)/Domain management/SubmitEmailVerification.md#)|acs:domain:\*:$accountid:\* |

|API|Authorization action|Authorization Resource|
|:--|:-------------------|:---------------------|
|\*|domain:\*|acs:domain:\*:$accountid:\*|

