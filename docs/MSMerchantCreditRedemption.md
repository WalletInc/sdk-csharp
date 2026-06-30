# WalletInc.Model.MSMerchantCreditRedemption

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TransactionID** | **string** | The transaction ID at the POS | 
**TransactionType** | **string** | The type of the transaction - either redemption or refund | 
**Amount** | **int** | The number of amount involved in this transaction | 
**RegisterID** | [**PickVSStaticVoucherExcludeKeyofVSStaticVoucherRedeemedAtOrRefundedAtOrLastViewedAtRegisterID**](PickVSStaticVoucherExcludeKeyofVSStaticVoucherRedeemedAtOrRefundedAtOrLastViewedAtRegisterID.md) |  | [optional] 
**TerminalType** | **string** | The type of the terminal | 
**Id** | **string** | The UUID of this record | 
**MerchantCreditID** | **string** | A 10 character alphanumeric unique value that represents each merchant credit record | 
**MerchantID** | **string** | The id of the merchant registered in WalletInc&#39;s database | 
**CreatedAt** | **DateTime** | The timestamp of when this resource was created | 
**IsActive** | **bool** | Denotes if this resource is active | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

