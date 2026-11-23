# WalletInc.Model.WTPointsLedgerEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**EntryType** | **WTPointsLedgerEntryType** |  | 
**Points** | **double** | Signed: positive adds to the balance, negative takes from it. | 
**Source** | **string** |  | 
**SourceLabel** | **string** | A plain-words label for &#x60;source&#x60;, ready to show. | 
**CreatedAt** | **DateTime** |  | 
**EmployeeName** | **string** |  | 
**Reason** | **string** |  | 
**EligibleAmountCents** | **double** |  | 
**BalanceAfter** | **double** | The balance after this entry. Present only when the membership service supplies it. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

