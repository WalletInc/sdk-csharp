# WalletInc.Model.ProductKey
Product update (\"What's New\") entries for the in-product News widget (KAN-557).  DESIGN - fan-out at write time, never read ReadMe here:    The release process writes each release to TWO sinks: ReadMe (the external wallet.dev surface)    and a structured store WE own (what this class reads). The in-product widget reads THIS store,    never ReadMe, which answers the two concerns directly:      - ReadMe outages cannot affect the merchant widget. ReadMe is a WRITE-TIME sink only, and that        write is already best-effort/non-fatal. Read time has zero external dependency.      - Nothing parses changelog markdown at read time. Entries are already structured (title +        items[]). The only split-into-items happens once, at WRITE time, on our OWN generated        release notes (semantic-release's \"* item\" list) - deterministic input we control, not a        regex over arbitrary third-party content.  STORE: the durable store is the Parse `ProductUpdate` class (KAN-557; chosen over a capped Redis list so entries survive a cache flush and can be curated/edited without a deploy). The one-time backfill and (later) the release fan-out write structured rows via `create`; `readFromStore` reads them. Everything else here - type/product filtering, read-through caching, the unread-count - sits behind `readFromStore`, so the store choice does not ripple into the endpoint or the widget.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

