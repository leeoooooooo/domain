# API Overview {#concept_xt1_n2b_b2b .concept}

The following tables list API operations that allow you to purchase, renew, and manage domains and to query the domain list and domain information. The management functions include modifying domain information, changing DNS servers, creating DNS servers, and managing registrant profiles.

## Domain management operations {#section_z25_r2b_b2b .section}

|Operation|Description|
|:--------|:----------|
|[QueryDomainList](reseller.en-US/API Reference (New)/Domain management/QueryDomainList.md#)|Queries the domain list under your account.|
|[QueryDomainByInstanceId](reseller.en-US/API Reference (New)/Domain management/QueryDomainByInstanceId.md#)|Queries the domain information under your account.|
|[QueryContactInfo](reseller.en-US/API Reference (New)/Domain management/QueryContactInfo.md#)|Queries the contact information of a domain.|
|[QueryChangeLogList](reseller.en-US/API Reference (New)/Domain management/QueryChangeLogList.md#)|Queries the operation logs of a domain.|
|[DeleteEmailVerification](reseller.en-US/API Reference (New)/Domain management/DeleteEmailVerification.md#)|Deletes verified email addresses.|
|[VerifyEmail](reseller.en-US/API Reference (New)/Domain management/VerifyEmail.md#)|Verifies email addresses.|
|[ListEmailVerification](reseller.en-US/API Reference (New)/Domain management/ListEmailVerification.md#)|Queries the verified email addresses.|
|[ResendEmailVerification](reseller.en-US/API Reference (New)/Domain management/ResendEmailVerification.md#)|Resends the verification email.|
|[SubmitEmailVerification](reseller.en-US/API Reference (New)/Domain management/SubmitEmailVerification.md#)|Sends email addresses for verification.|
|[SaveSingleTaskForCreatingOrderActivate](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderActivate.md#)|Submits a task for registering a domain.|
|[SaveSingleTaskForCreatingOrderRenew](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderRenew.md#)|Submits a task for renewing a domain.|
|[SaveBatchTaskForModifyingDomainDns](reseller.en-US/API Reference (New)/Domain management/SaveBatchTaskForModifyingDomainDns.md#)|Submits a batch task for changing the DNS servers of domains.|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](reseller.en-US/API Reference (New)/Domain management/Submit a batch task for modifying domain name information by new registrant.md#)|Submits a batch task for updating the contact information of domains to the name and credentials of a new contact person.|
|[SaveBatchTaskForCreatingOrderActivate](reseller.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderActivate.md#)|Submits a batch task for registering domains.|
|[SaveBatchTaskForCreatingOrderRenew](reseller.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderRenew.md#)|Submits a batch task for renewing domains.|
|[SaveBatchTaskForUpdateProhibitionLock](reseller.en-US/API Reference (New)/Domain management/SaveBatchTaskForUpdateProhibitionLock.md#)|Submits a batch task for setting the update prohibition lock for domains.|
|[SaveBatchTaskForTransferProhibitionLock](reseller.en-US/API Reference (New)/Domain management/SaveBatchTaskForTransferProhibitionLock.md#)|Submits a batch task for setting the transfer prohibition lock for domains.|
|[QueryTaskList](reseller.en-US/API Reference (New)/Domain management/QueryTaskList.md#)|Queries domain tasks.|
|[QueryTaskInfoHistory](reseller.en-US/API Reference (New)/Domain management/QueryTaskInfoHistory.md#)|Queries the historical domain tasks.|
|[QueryTaskDetailList](reseller.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#)|Queries details about domain tasks.|
|[QueryTaskDetailHistory](reseller.en-US/API Reference (New)/Domain management/QueryTaskDetailHistory.md#)|Queries details about historical domain tasks.|
|[CheckDomain](reseller.en-US/API Reference (New)/Domain management/CheckDomain.md#)|Checks whether a domain can be registered.|
|[AcknowledgeTaskResult](reseller.en-US/API Reference (New)/Domain management/AcknowledgeTaskResult.md#)|Acknowledges task details.|
|[CheckTransferInFeasibility](reseller.en-US/API Reference (New)/Domain management/CheckTransferInFeasibility.md#)|Checks whether a domain can be transferred to Alibaba Cloud.|
|[PollTaskResult](reseller.en-US/API Reference (New)/Domain management/PollTaskResult.md#)|Queries details about executed tasks.|
|[QueryTransferInByInstanceId](reseller.en-US/API Reference (New)/Domain management/QueryTransferInByInstanceId.md#)|Queries the transfer-in records of domains in an instance.|
|[QueryTransferInList](reseller.en-US/API Reference (New)/Domain management/QueryTransferInList.md#)|Queries the domain transfer-in list.|
|[QueryTransferOutInfo](reseller.en-US/API Reference (New)/Domain management/QueryTransferOutInfo.md#)|Queries the transfer-out information of a domain.|
|[SaveSingleTaskForCancelingTransferIn](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferIn.md#)|Submits a task for canceling the transfer-in of a domain.|
|[SaveSingleTaskForCancelingTransferOut](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferOut.md#)|Submits a task for canceling the transfer-out of a domain.|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForQueryingTransferAuthorizationCode.md#)|Submits a task for querying the domain transfer code.|
|[TransferInCheckMailToken](reseller.en-US/API Reference (New)/Domain management/TransferInCheckMailToken.md#)|Verifies the token received in the email box of a registrant.|
|[TransferInReenterTransferAuthorizationCode](reseller.en-US/API Reference (New)/Domain management/TransferInReenterTransferAuthorizationCode.md#)|Enters the transfer code again to transfer the domain to Alibaba Cloud.|
|[TransferInRefetchWhoisEmail](reseller.en-US/API Reference (New)/Domain management/TransferInRefetchWhoisEmail.md#)|Fetches the registrant's email address from WHOIS again for a domain to be transferred to Alibaba Cloud.|
|[TransferInResendMailToken](reseller.en-US/API Reference (New)/Domain management/TransferInResendMailToken.md#)|Resends the verification email for a domain to be transferred to Alibaba Cloud.|
|[VerifyContactField](reseller.en-US/API Reference (New)/Domain management/VerifyContactField.md#)|Verifies the contact information of a domain.|
|[SaveSingleTaskForCreatingOrderRedeem](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderRedeem.md#)|Submits a task for redeeming a domain.|
|[SaveBatchTaskForCreatingOrderRedeem](reseller.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderRedeem.md#)|Submits a batch task for redeeming domains.|
|[SaveSingleTaskForCreatingDnsHost](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingDnsHost.md#)|Submits a task for creating a DNS host.|
|[SaveSingleTaskForModifyingDnsHost](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForModifyingDnsHost.md#)|Submits a task for changing a DNS host.|
|[SaveSingleTaskForSynchronizingDnsHost](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForSynchronizingDnsHost.md#)|Submits a task for synchronizing DNS host information.|
|[SaveSingleTaskForTransferProhibitionLock](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForTransferProhibitionLock.md#)|Submits a task for setting the transfer prohibition lock for a domain.|
|[SaveSingleTaskForUpdateProhibitionLock](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdateProhibitionLock.md#)|Submits a task for setting the update prohibition lock for a domain.|
|[SaveSingleTaskForUpdatingContactInfo](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdatingContactInfo.md#)|Submits a task for modifying information about a domain.|
|[QueryDnsHost](reseller.en-US/API Reference (New)/Domain management/QueryDnsHost.md#)|Queries the DNS host of a domain.|
|[SaveSingleTaskForAddingDSRecord](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForAddingDSRecord.md#)|Submits a task for creating a DS record.|
|[SaveSingleTaskForModifyingDSRecord](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForModifyingDSRecord.md#)|Submits a task for modifying a DS record.|
|[SaveSingleTaskForDeletingDSRecord](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForDeletingDSRecord.md#)|Submits a task for deleting a DS record.|
|[SaveSingleTaskForSynchronizingDSRecord](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForSynchronizingDSRecord.md#)|Submits a task for synchronizing DS records.|
|[SaveSingleTaskForAssociatingEns](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForAssociatingEns.md#)|Submits a task for associating an Ethereum wallet address with a domain.|
|[QueryEnsAssociation](reseller.en-US/API Reference (New)/Domain management/QueryEnsAssociation.md#)|Queries the Ethereum wallet addresses associated with domains in Ethereum Name Service \(ENS\).|
|[QueryDSRecord](reseller.en-US/API Reference (New)/Domain management/QueryDSRecord.md#)|Queries the DS records of a domain.|
|[QueryDomainByDomainName](reseller.en-US/API Reference (New)/Domain management/QueryDomainByDomainName.md#)|Queries information about a specific domain.|
|[SaveSingleTaskForDisassociatingEns](reseller.en-US/API Reference (New)/Domain management/SaveSingleTaskForDisassociatingEns.md#)|Submits a task for disassociating an Ethereum wallet address from a domain.|
|[QueryLocalEnsAssociation](reseller.en-US/API Reference (New)/Domain management/QueryLocalEnsAssociation.md#)|Queries the Ens-associated addresses recorded in Alibaba Cloud.|
|[SaveSingleTaskForSaveArtExtension](reseller.en-US/.md#)|Submits a task for configuring the extension information about an .art domain.|
|[QueryArtExtension](reseller.en-US/.md#)|Queries the extension information about an .art domain.|

## Registrant profile operations {#section_zdt_d3b_b2b .section}

|Operation|Description|
|:--------|:----------|
|[SaveRegistrantProfile](reseller.en-US/API Reference (New)/Information template/SaveRegistrantProfile.md#)|Creates or saves a registrant profile.|
|[QueryRegistrantProfiles](reseller.en-US/API Reference (New)/Information template/QueryRegistrantProfiles.md#)|Queries the registrant profiles under your account.|
|[DeleteRegistrantProfile](reseller.en-US/API Reference (New)/Information template/DeleteRegistrantProfile.md#)|Deletes a registrant profile.|

