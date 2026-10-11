# WalletInc.Model.WTCustomDomain

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Hostname** | **string** | The custom domain, or empty when none is set up. | 
**State** | **WTCustomDomainState** | Where the domain is in its setup. Absent when &#x60;hostname&#x60; is empty. | [optional] 
**Managed** | **bool** | False when Wallet set the domain up by hand. Such a domain is shown read-only and cannot be changed here. | 
**DnsTarget** | **string** | The CNAME target the merchant points their domain at. | 
**Txt** | [**WTCustomDomainTXT**](WTCustomDomainTXT.md) | Present when the merchant must also add a TXT record. | [optional] 
**Error** | [**WTCustomDomainError**](WTCustomDomainError.md) | Present when &#x60;state&#x60; is &#x60;error&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

