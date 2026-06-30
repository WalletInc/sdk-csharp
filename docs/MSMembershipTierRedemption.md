# WalletInc.Model.MSMembershipTierRedemption

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MemberID** | **string** | A 10 character alphanumeric unique value that represents each member | 
**TransactionID** | **string** | The transaction ID at the POS | 
**TransactionType** | **string** | The type of the transaction - either redemption or refund | 
**Amount** | **int** | The amount that has been redeemed, in cents | 
**RegisterID** | [**PickVSStaticVoucherExcludeKeyofVSStaticVoucherRedeemedAtOrRefundedAtOrLastViewedAtRegisterID**](PickVSStaticVoucherExcludeKeyofVSStaticVoucherRedeemedAtOrRefundedAtOrLastViewedAtRegisterID.md) |  | [optional] 
**TerminalType** | **string** | The type of the terminal | 
**Id** | **string** | The UUID of this record | 
**TierID** | **string** | A 10 character alphanumeric unique value that represents each membership tier | 
**MerchantID** | **string** | The id of the merchant registered in WalletInc&#39;s database | 
**CreatedAt** | **DateTime** | The timestamp of when this resource was created | 
**IsActive** | **bool** | Denotes if this resource is active | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

