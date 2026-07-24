# WalletInc.Model.ProductUpdateIngestBody
The structured release entry CI posts. Mirrors ProductUpdateEntry, with publishedAt optional (defaults to now).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Product** | **ProductKey** | Which product shipped: \&quot;admin_portal\&quot; (shown in the merchant widget) or \&quot;api\&quot;. | 
**VarVersion** | **string** | The release version, e.g. \&quot;2.4.0\&quot;. Metadata; the widget renders title + items. | 
**Type** | **ProductUpdateType** | \&quot;added\&quot; for a feature release, \&quot;fixed\&quot; for a patch. | 
**Title** | **string** | Merchant-facing headline for the release. | 
**Items** | **List&lt;string&gt;** | The release-note bullets, already split by the caller. | 
**PublishedAt** | **string** | ISO 8601. Optional; defaults to the ingest time. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

