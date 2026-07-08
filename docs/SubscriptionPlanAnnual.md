# WalletInc.Model.SubscriptionPlanAnnual
Annual pricing for the monthly/annual billing toggle. Optional. When a plan factory defines it, `id` is the REAL annual Stripe price id and is chargeable via `/v2/billing/plan` with `billingCadence: \"annual\"`. When absent, non-prod environments receive a PLACEHOLDER from PlanCatalog.withAnnualPlaceholder() (id prefixed `price_ANNUAL_PLACEHOLDER_`), which MUST NOT be used at checkout and is rejected there.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Price** | **double** |  | 
**Id** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

