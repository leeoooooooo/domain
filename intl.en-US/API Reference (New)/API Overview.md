# API Overview {#concept_xt1_n2b_b2b .concept}

The domain name management APIs can be used to buy, renew, redeem, and manage \(including information modification, DNS modification, DNS creation, and information template management\) domain names, and query domain name lists and domain name information.

## Domain name management APIs {#section_z25_r2b_b2b .section}

|API|Description|
|:--|:----------|
|[QueryDomainList](intl.en-US/API Reference (New)/Domain management/QueryDomainList.md#)|Query the list of domain names under the current account.|
|[QueryDomainByInstanceId](intl.en-US/API Reference (New)/Domain management/QueryDomainByInstanceId.md#)|Query the domain name information under the current account.|
|[QueryContactInfo](intl.en-US/API Reference (New)/Domain management/QueryContactInfo.md#)|Query the contact information for the domain name.|
|[QueryChangeLogList](intl.en-US/API Reference (New)/Domain management/QueryChangeLogList.md#)|Query operation logs.|
|[DeleteEmailVerification](intl.en-US/API Reference (New)/Domain management/DeleteEmailVerification.md#)|Delete an email address verification task.|
|[VerifyEmail](intl.en-US/API Reference (New)/Domain management/VerifyEmail.md#)|Verify email address.|
|[ListEmailVerification](intl.en-US/API Reference (New)/Domain management/ListEmailVerification.md#)|Query the list of email address verification tasks.|
|[ResendEmailVerification](intl.en-US/API Reference (New)/Domain management/ResendEmailVerification.md#)|Resend the verification email.|
|[SubmitEmailVerification](intl.en-US/API Reference (New)/Domain management/SubmitEmailVerification.md#)|Submit email address authentication list|
|[SaveSingleTaskForCreatingOrderActivate](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderActivate.md#)|Submit a domain name registration task.|
|[SaveSingleTaskForCreatingOrderRenew](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderRenew.md#)|Submit a domain name review task.|
|[SaveBatchTaskForModifyingDomainDns](intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForModifyingDomainDns.md#)|Submit a bulk domain names DNS modification task.|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](intl.en-US/API Reference (New)/Domain management/Submit a batch task for modifying domain name information by new registrant.md#)|Submit a modifying registered contact information by new contact information task for bulk domain names.|
|[SaveBatchTaskForCreatingOrderActivate](intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderActivate.md#)|Submit a bulk domain names registration task.|
|[SaveBatchTaskForCreatingOrderRenew](intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderRenew.md#)| Submit a bulk domain names renewal task.|
|[SaveBatchTaskForUpdateProhibitionLock](intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForUpdateProhibitionLock.md#)|Submit a bulk domain names prohibition lock update task.|
|[SaveBatchTaskForTransferProhibitionLock](intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForTransferProhibitionLock.md#)| Submit a bulk domain names transfer prohibition lock task.|
|[QueryTaskList](intl.en-US/API Reference (New)/Domain management/QueryTaskList.md#)|Query the domain name task list.|
|[QueryTaskInfoHistory](intl.en-US/API Reference (New)/Domain management/QueryTaskInfoHistory.md#)|Query the historical task list for a domain name.|
|[QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#)|Query the details list of a domain name task.|
|[QueryTaskDetailHistory](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailHistory.md#)|Query the historical task detail list for a domain name.|
|[CheckDomain](intl.en-US/API Reference (New)/Domain management/CheckDomain.md#)|Check whether the domain name can be registered.|
|[AcknowledgeTaskResult](intl.en-US/API Reference (New)/Domain management/AcknowledgeTaskResult.md#)|Check a task result.|
|[CheckTransferInFeasibility](intl.en-US/API Reference (New)/Domain management/CheckTransferInFeasibility.md#)|Check whether the domain name can be transferred in.|
|[PollTaskResult](intl.en-US/API Reference (New)/Domain management/PollTaskResult.md#)|Query details list for completed tasks.|
|[QueryTransferInByInstanceId](intl.en-US/API Reference (New)/Domain management/QueryTransferInByInstanceId.md#)|Query domain name transfer in information by instance ID.|
|[QueryTransferInList](intl.en-US/API Reference (New)/Domain management/QueryTransferInList.md#)| Query the domain name transfer in list.|
|[QueryTransferOutInfo](intl.en-US/API Reference (New)/Domain management/QueryTransferOutInfo.md#)|Query the domain name transfer out list.|
|[SaveSingleTaskForCancelingTransferIn](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferIn.md#)|Submit a canceling domain name transfer in task.|
|[SaveSingleTaskForCancelingTransferOut](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferOut.md#)| Submit a canceling domain name transfer out task.|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForQueryingTransferAuthorizationCode.md#)|Submit a obtaining domain name transfer authorization code task.|
|[TransferInCheckMailToken](intl.en-US/API Reference (New)/Domain management/TransferInCheckMailToken.md#)|Verification email for domain name transfer in.|
|[TransferInReenterTransferAuthorizationCode](intl.en-US/API Reference (New)/Domain management/TransferInReenterTransferAuthorizationCode.md#)|Reenter the authorization code for domain name transfer in.|
|[TransferInRefetchWhoisEmail](intl.en-US/API Reference (New)/Domain management/TransferInRefetchWhoisEmail.md#)|Re-fetch the WHOIS email for domain name transfer in.|
|[TransferInResendMailToken](intl.en-US/API Reference (New)/Domain management/TransferInResendMailToken.md#)|Resend the verification email for domain name transfer in.|
|[VerifyContactField](intl.en-US/API Reference (New)/Domain management/VerifyContactField.md#)|Verify contact information.|
|[SaveSingleTaskForCreatingOrderRedeem](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderRedeem.md#)|Submit a domain name redemption task.|
|[SaveBatchTaskForCreatingOrderRedeem](intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderRedeem.md#)|Submit a bulk domain names redemption task.|
|[SaveSingleTaskForCreatingDnsHost](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingDnsHost.md#)| Submit a DNS host creation task.|
|[SaveSingleTaskForModifyingDnsHost](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForModifyingDnsHost.md#)| Submit a DNS host modification task.|
|[SaveSingleTaskForSynchronizingDnsHost](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForSynchronizingDnsHost.md#)| Submit a DNS host sync task.|
|[SaveSingleTaskForTransferProhibitionLock](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForTransferProhibitionLock.md#)|Submit a transfer prohibition lock task.|
|[SaveSingleTaskForUpdateProhibitionLock](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdateProhibitionLock.md#)| Submit a update prohibition lock task.|
|[SaveSingleTaskForUpdatingContactInfo](intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdatingContactInfo.md#)| Submit a domain name information modification task.|
|[QueryDnsHost](intl.en-US/API Reference (New)/Domain management/QueryDnsHost.md#)| Query the domain name DNS host.|

## Information template APIs {#section_zdt_d3b_b2b .section}

|API|Description|
|:--|:----------|
|[SaveRegistrantProfile](intl.en-US/API Reference (New)/Information template/SaveRegistrantProfile.md#)|Create or save a domain name information template.|
|[QueryRegistrantProfiles](intl.en-US/API Reference (New)/Information template/QueryRegistrantProfiles.md#)|Query the domain name information templates under the current account.|
|[DeleteRegistrantProfile](intl.en-US/API Reference (New)/Information template/DeleteRegistrantProfile.md#)|Delete the specified domain name information template.|

