# WalletInc.Model.PickMSMemberExcludeKeyofMSMemberMemberIdentifier
From T, pick a set of properties whose keys are in the union K

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | A 10 character alphanumeric unique value that represents each member | 
**MerchantID** | **string** | The id of the merchant registered in WalletInc&#39;s database | 
**CreatedAt** | **DateTime** | The timestamp of when this resource was created | 
**UpdatedAt** | **DateTime** | The timestamp of when this resource was updated | 
**IsActive** | **bool** | Denotes if this resource is active | 
**FirstName** | **string** | An optional first name of the member | [optional] 
**LastName** | **string** | An optional last name of the member | [optional] 
**MembershipTierID** | **string** | The object ID of the membership tier that this member belongs to | 
**MobileNumber** | **string** |  | 
**Email** | **string** |  | 
**Birthday** | **string** | Represents the date of birth of the member. Defaults to 0000-00-00, which represents that the date of birth has not been configured | 
**PointsAccrued** | **int** | The number of points that the member has accrued | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

