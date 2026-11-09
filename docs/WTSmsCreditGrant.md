# WalletInc.Model.WTSmsCreditGrant
KAN-463: the SMS credit ledger. Grants are in SEGMENTS, the unit Twilio bills.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The grant&#39;s id. | 
**MerchantID** | **string** |  | 
**Segments** | **double** | Segments added (negative only for an adjustment). | 
**Source** | **string** | \&quot;purchase\&quot;, \&quot;bonus\&quot; or \&quot;adjustment\&quot;. | 
**Note** | **string** | Why it was granted (required for a bonus or an adjustment). | [optional] 
**Reference** | **string** | The purchase it came from, e.g. a Stripe payment id, when there is one. | [optional] 
**GrantedBy** | **string** | The Wallet staff user, or \&quot;system\&quot;, that made the grant. | 
**CreatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

