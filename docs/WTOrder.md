# WalletInc.Model.WTOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | [**AmenityId**](AmenityId.md) |  | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**MerchantID** | **string** | The merchant the order was placed with. | 
**MemberID** | **string** |  | [optional] 
**MobileNumber** | **string** |  | [optional] 
**Status** | **OrderStatus** |  | 
**Currency** | **string** |  | 
**AmountTotal** | **int** |  | 
**StripeCheckoutSessionID** | **string** |  | [optional] 
**StripePaymentIntentID** | **string** |  | [optional] 
**StripeChargeID** | **string** |  | [optional] 
**ReceiptURL** | **string** |  | [optional] 
**AcquisitionSource** | **string** |  | [optional] 
**ShareId** | **string** |  | [optional] 
**LineItems** | [**List&lt;WTOrderLineItem&gt;**](WTOrderLineItem.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

