# WalletInc.Model.WTCurrentMerchantTermsVersion
One in-force merchant agreement, as a signup page needs it.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DocumentType** | **MerchantTermsDocumentType** | Which agreement: \&quot;tos\&quot; or \&quot;privacy\&quot;. | 
**VersionId** | **string** | The exact id to send back as &#x60;acceptedTermsVersion&#x60; / &#x60;acceptedPrivacyVersion&#x60; on registration. | 
**EffectiveDate** | **string** | When this version came into force. | 
**Url** | **string** | The document the merchant should be shown and link to. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

