# WalletInc.Model.CSPViolationSummaryRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ViolatedDirective** | **string** |  | 
**BlockedHost** | **string** | The scheme+host of the blocked URI, or the raw value for schemeless blocks (inline / eval / data:). | 
**Disposition** | **string** | \&quot;enforce\&quot; (actually blocked) vs \&quot;report\&quot; (report-only twin). | 
**Count** | **int** |  | 
**SampleDocumentURI** | **string** |  | 
**FirstSeen** | **DateTime** |  | [optional] 
**LastSeen** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

