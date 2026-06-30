# WalletInc.Model.PresignedPostFields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Policy** | **string** | A base64-encoded policy detailing what constitutes an acceptable POST upload. Composed of the conditions and expiration provided to s3.createPresignedPost | 
**XAmzSignature** | **string** | A hex-encoded HMAC of the POST policy, signed with the credentials provided to the S3 client. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

