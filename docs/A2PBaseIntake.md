# WalletInc.Model.A2PBaseIntake
Fields shared by every entity intake. Conditional fields (stock, brand contact email) are re-added per type.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FirstName** | **string** |  | 
**LastName** | **string** |  | 
**Email** | **string** |  | 
**BusinessClassification** | **BusinessClassification** |  | 
**BusinessIndustry** | **BusinessIndustry** |  | 
**TaxIDType** | **BusinessRegistrationIdentifier** |  | 
**TaxID** | **string** |  | 
**WebsiteURL** | **string** |  | 
**SocialMediaURL** | **string** |  | 
**RegionsOfOperation** | [**List&lt;BusinessRegionsOfOperation&gt;**](BusinessRegionsOfOperation.md) |  | 
**MessagingVolumeHigh** | **bool** |  | 
**JobTitle** | **string** |  | 
**JobPosition** | **JobPosition** |  | 
**BillingConsent** | [**A2PBillingConsent**](A2PBillingConsent.md) |  | [optional] 
**BusinessName** | **string** |  | 
**BusinessType** | **BusinessType** |  | 
**Address1** | **string** |  | 
**Address2** | **string** |  | [optional] 
**City** | **string** |  | 
**State** | **string** |  | 
**PostalCode** | **string** |  | 
**Country** | **string** |  | 
**PhoneNumber** | **string** |  | 
**IsTwilioTermsRead** | **bool** |  | 
**IsWalletSmsTermsRead** | **bool** |  | 
**IsPricingUnderstood** | **bool** |  | 
**IsPrivacyAndTosPresent** | **bool** |  | 
**PrivacyPolicyUrl** | **string** |  | [optional] 
**WillObtainConsent** | **bool** |  | 
**WillHonorOptOut** | **bool** |  | 
**WillFollowContentRules** | **bool** |  | 
**WillComplyLawAndHours** | **bool** |  | 
**InfoIsAccurate** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

