# WalletInc.Model.WTPointsAwardResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Skipped** | **WTPointsSkipReason** | Present only when nothing was awarded; the other fields are then absent. | [optional] 
**EntryID** | **string** |  | [optional] 
**PointsAwarded** | **double** |  | [optional] 
**Balance** | **double** |  | [optional] 
**LifetimeEarned** | **double** |  | [optional] 
**Earned12Months** | **double** |  | [optional] 
**PreviousTierID** | **string** |  | [optional] 
**NewTierID** | **string** |  | [optional] 
**TierChanged** | **bool** |  | [optional] 
**NewTierName** | **string** | The new tier&#39;s name, set only when the award moved the member up a tier. | [optional] 
**Replayed** | **bool** | True when this answer repeats an earlier award with the same idempotency key. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

