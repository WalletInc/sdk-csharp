# WalletInc.Model.WTSmsCreditSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MerchantID** | **string** |  | 
**IsOnLedger** | **bool** | False until the merchant&#39;s first grant: until then sends use the legacy MaxSMSCount ceiling. | 
**CreditsGranted** | **double** | Total segments ever granted (purchases, bonuses and adjustments). | 
**CreditOverdraft** | **double** |  | 
**LedgerEpoch** | **string** | The first grant&#39;s time; usage before it never counts against the ledger. | [optional] 
**Grants** | [**List&lt;WTSmsCreditGrant&gt;**](WTSmsCreditGrant.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

