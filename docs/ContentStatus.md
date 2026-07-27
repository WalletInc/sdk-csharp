# WalletInc.Model.ContentStatus
Curation gate for the merchant-facing feed.   - \"hold\": ingested but NOT shown to merchants. The default for everything the release fan-out writes,     so raw commit language / a not-yet-live feature can never reach the widget on its own. Marketing     (and Legal where needed) rewrite the entry into merchant copy, then flip it to \"ready\".   - \"ready\": curated and cleared; shown in the widget. A row with NO ContentStatus (legacy rows written before this gate) is grandfathered as visible: only an explicit \"hold\" hides. So the gate is fail-safe for NEW writes (default hold) without emptying the feed of the already-curated backfill.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

