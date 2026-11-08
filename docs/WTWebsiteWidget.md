# WalletInc.Model.WTWebsiteWidget
What the portal's install page needs: who may embed, where the snippet loads from, and what it loads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Origins** | **List&lt;string&gt;** | The website origins allowed to embed this merchant&#39;s wallet, normalised (&#x60;https://&#x60; plus host, lowercase). | 
**WalletHost** | **string** | Where the snippet loads the wallet from: the merchant&#39;s live custom domain, otherwise this environment&#39;s default wallet site. | 
**WalletID** | **string** | The id of the merchant&#39;s wallet configuration, the object the widget opens. | 
**MarkRemovable** | **bool** | True when the merchant&#39;s plan includes White-Labeled Custom Domain, which removes the \&quot;Powered by Wallet\&quot; mark. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

