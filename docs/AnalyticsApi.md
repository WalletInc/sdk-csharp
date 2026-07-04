# WalletInc.Api.AnalyticsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CountAllSubscribers**](AnalyticsApi.md#countallsubscribers) | **GET** /v2/analytics/sms/all/subscribers/count | Count opt in list subscribers |
| [**CountAuthenticatedSessions**](AnalyticsApi.md#countauthenticatedsessions) | **GET** /v2/analytics/walletPageViews/sessions/count/distinct/authenticated | Count authenticated sessions |
| [**CountDistinctRedemptions**](AnalyticsApi.md#countdistinctredemptions) | **GET** /v2/analytics/ledger/paymentObject/distinct/count | Count distinct payment object redemptions |
| [**CountHelpDeskRequests**](AnalyticsApi.md#counthelpdeskrequests) | **GET** /v2/analytics/helpdeskrequests/count | Count help desk requests |
| [**CountInboundMessages**](AnalyticsApi.md#countinboundmessages) | **GET** /v2/analytics/sms/inbound/count | Count inbound SMS messages |
| [**CountNewSessions**](AnalyticsApi.md#countnewsessions) | **GET** /v2/analytics/walletPageViews/sessions/count/distinct/first | Count new sessions |
| [**CountOptInListSubscribersPartitionedByDate**](AnalyticsApi.md#countoptinlistsubscriberspartitionedbydate) | **GET** /v2/analytics/sms/all/subscribers/count/date | Count opt in list subscribers by date |
| [**CountOutboundMessages**](AnalyticsApi.md#countoutboundmessages) | **GET** /v2/analytics/sms/outbound/count | Count outbound SMS messages |
| [**CountTotalSessions**](AnalyticsApi.md#counttotalsessions) | **GET** /v2/analytics/walletPageViews/sessions/count/distinct | Count total sessions |
| [**CountTransactions**](AnalyticsApi.md#counttransactions) | **GET** /v2/analytics/ledger/transactions/count | Count ledger transactions |
| [**CountVerifiedWalletPageViews**](AnalyticsApi.md#countverifiedwalletpageviews) | **GET** /v2/analytics/walletPageViews/sessions/verified/distinct/walletObjectsCount | Get wallet object counts within a given time frame that have a valid phone verification token |
| [**CountWalletPageViews**](AnalyticsApi.md#countwalletpageviews) | **GET** /v2/analytics/walletPageViews/sessions/distinct/walletObjectsCount | Get wallet object counts within a given time frame |
| [**ExitLinkSummary**](AnalyticsApi.md#exitlinksummary) | **GET** /v2/analytics/walletPageViews/exitLinkSummary | Count exit clicks |
| [**FetchAnalyticsAdCreditsCountPartitionedByEmployee**](AnalyticsApi.md#fetchanalyticsadcreditscountpartitionedbyemployee) | **GET** /v2/analytics/advertisementCredits/count/employee | Count ad credits by employee |
| [**FetchAnalyticsAdCreditsCountPartitionedByPaymentDesign**](AnalyticsApi.md#fetchanalyticsadcreditscountpartitionedbypaymentdesign) | **GET** /v2/analytics/advertisementCredits/count/paymentDesign | Count ad credits by payment design |
| [**FetchAnalyticsAdCreditsCountPartitionedByValueType**](AnalyticsApi.md#fetchanalyticsadcreditscountpartitionedbyvaluetype) | **GET** /v2/analytics/advertisementCredits/count/valueType | Count ad credits by value type |
| [**FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditID**](AnalyticsApi.md#fetchanalyticsadcreditsredemptionsamountpartitionedbyadcreditid) | **GET** /v2/analytics/advertisementCredits/redemptions/amount/adCredit | Get redemption amount of ad credits by Ad Credit |
| [**FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsadcreditsredemptionsamountpartitionedbydate) | **GET** /v2/analytics/advertisementCredits/redemptions/amount/date | Get redemption amount of ad credits by date |
| [**FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditID**](AnalyticsApi.md#fetchanalyticsadcreditsredemptionscountpartitionedbyadcreditid) | **GET** /v2/analytics/advertisementCredits/redemptions/count/adCredit | Count redemptions of ad credits by Ad Credit |
| [**FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsadcreditsredemptionscountpartitionedbydate) | **GET** /v2/analytics/advertisementCredits/redemptions/count/date | Count redemptions of ad credits by date |
| [**FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditID**](AnalyticsApi.md#fetchanalyticsadcreditsrefundsamountpartitionedbyadcreditid) | **GET** /v2/analytics/advertisementCredits/refunds/amount/adCredit | Get refund amount of ad credits by Ad Credit |
| [**FetchAnalyticsAdCreditsRefundsAmountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsadcreditsrefundsamountpartitionedbydate) | **GET** /v2/analytics/advertisementCredits/refunds/amount/date | Get refund amount of ad credits by date |
| [**FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditID**](AnalyticsApi.md#fetchanalyticsadcreditsrefundscountpartitionedbyadcreditid) | **GET** /v2/analytics/advertisementCredits/refunds/count/adCredit | Count refunds of ad credits by Ad Credit |
| [**FetchAnalyticsAdCreditsRefundsCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsadcreditsrefundscountpartitionedbydate) | **GET** /v2/analytics/advertisementCredits/refunds/count/date | Count refunds of ad credits by date |
| [**FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditID**](AnalyticsApi.md#fetchanalyticsadcreditsscanscountpartitionedbyadcreditid) | **GET** /v2/analytics/advertisementCredits/scans/count/adCredit | Count scans of ad credits by Ad Credit |
| [**FetchAnalyticsAdCreditsScansCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsadcreditsscanscountpartitionedbydate) | **GET** /v2/analytics/advertisementCredits/scans/count/date | Count scans of ad credits by date |
| [**FetchAnalyticsCampaignWalletPageViews**](AnalyticsApi.md#fetchanalyticscampaignwalletpageviews) | **GET** /v2/analytics/walletPageViews/campaign/{campaignID} | Get a campaign&#39;s wallet page views |
| [**FetchAnalyticsCampaignsCountPartitionedByCampaignID**](AnalyticsApi.md#fetchanalyticscampaignscountpartitionedbycampaignid) | **GET** /v2/analytics/campaigns/count/campaign/created | Count created campaigns by campaign |
| [**FetchAnalyticsCampaignsCountPartitionedByEmployee**](AnalyticsApi.md#fetchanalyticscampaignscountpartitionedbyemployee) | **GET** /v2/analytics/campaigns/count/employee | Count campaigns by employee |
| [**FetchAnalyticsCampaignsCountPartitionedByPaymentDesign**](AnalyticsApi.md#fetchanalyticscampaignscountpartitionedbypaymentdesign) | **GET** /v2/analytics/campaigns/count/paymentDesign | Count campaigns by payment design |
| [**FetchAnalyticsCampaignsCountPartitionedByValueType**](AnalyticsApi.md#fetchanalyticscampaignscountpartitionedbyvaluetype) | **GET** /v2/analytics/campaigns/count/valueType | Count campaigns by value type |
| [**FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignID**](AnalyticsApi.md#fetchanalyticscampaignsredemptionsamountpartitionedbycampaignid) | **GET** /v2/analytics/campaigns/redemptions/amount/campaign | Get redemption amount of campaigns by Campaign |
| [**FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDate**](AnalyticsApi.md#fetchanalyticscampaignsredemptionsamountpartitionedbydate) | **GET** /v2/analytics/campaigns/redemptions/amount/date | Get redemption amount of campaigns by date |
| [**FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignID**](AnalyticsApi.md#fetchanalyticscampaignsredemptionscountpartitionedbycampaignid) | **GET** /v2/analytics/campaigns/redemptions/count/campaign | Count redemptions of campaigns by Campaign |
| [**FetchAnalyticsCampaignsRedemptionsCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticscampaignsredemptionscountpartitionedbydate) | **GET** /v2/analytics/campaigns/redemptions/count/date | Count redemptions of campaigns by date |
| [**FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignID**](AnalyticsApi.md#fetchanalyticscampaignsrefundsamountpartitionedbycampaignid) | **GET** /v2/analytics/campaigns/refunds/amount/campaign | Get refund amount of campaigns by Campaign |
| [**FetchAnalyticsCampaignsRefundsAmountPartitionedByDate**](AnalyticsApi.md#fetchanalyticscampaignsrefundsamountpartitionedbydate) | **GET** /v2/analytics/campaigns/refunds/amount/date | Get refund amount of campaigns by date |
| [**FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignID**](AnalyticsApi.md#fetchanalyticscampaignsrefundscountpartitionedbycampaignid) | **GET** /v2/analytics/campaigns/refunds/count/campaign | Count refunds of campaigns by Campaign |
| [**FetchAnalyticsCampaignsRefundsCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticscampaignsrefundscountpartitionedbydate) | **GET** /v2/analytics/campaigns/refunds/count/date | Count refunds of campaigns by date |
| [**FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsdeliveredoutboundmessagescountpartitionedbydate) | **GET** /v2/analytics/outboundSMS/count/date/delivered | Count delivered outbound messages by date |
| [**FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumber**](AnalyticsApi.md#fetchanalyticsdeliveredoutboundmessagescountpartitionedbyphonenumber) | **GET** /v2/analytics/outboundSMS/count/phoneNumber/delivered | Count delivered outbound messages by phone number |
| [**FetchAnalyticsDistinctWalletSessions**](AnalyticsApi.md#fetchanalyticsdistinctwalletsessions) | **GET** /v2/analytics/walletPageViews/sessions/distinct | Get distinct wallet sessions |
| [**FetchAnalyticsDynamicVouchersCountPartitionedByEmployee**](AnalyticsApi.md#fetchanalyticsdynamicvoucherscountpartitionedbyemployee) | **GET** /v2/analytics/dynamicVouchers/count/employee | Count dynamic vouchers by employee |
| [**FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesign**](AnalyticsApi.md#fetchanalyticsdynamicvoucherscountpartitionedbypaymentdesign) | **GET** /v2/analytics/dynamicVouchers/count/paymentDesign | Count dynamic vouchers by payment design |
| [**FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsdynamicvouchersredemptionsamountpartitionedbydate) | **GET** /v2/analytics/dynamicVouchers/redemptions/amount/date | Get redemption amount of dynamic vouchers by date |
| [**FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherID**](AnalyticsApi.md#fetchanalyticsdynamicvouchersredemptionsamountpartitionedbydynamicvoucherid) | **GET** /v2/analytics/dynamicVouchers/redemptions/amount/dynamicVoucher | Get redemption amount of dynamic vouchers by dynamic voucher |
| [**FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsdynamicvouchersredemptionscountpartitionedbydate) | **GET** /v2/analytics/dynamicVouchers/redemptions/count/date | Count redemptions of dynamic vouchers by date |
| [**FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherID**](AnalyticsApi.md#fetchanalyticsdynamicvouchersredemptionscountpartitionedbydynamicvoucherid) | **GET** /v2/analytics/dynamicVouchers/redemptions/count/dynamicVoucher | Count redemptions of dynamic vouchers by dynamic voucher |
| [**FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsdynamicvouchersrefundsamountpartitionedbydate) | **GET** /v2/analytics/dynamicVouchers/refunds/amount/date | Get refund amount of dynamic vouchers by date |
| [**FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherID**](AnalyticsApi.md#fetchanalyticsdynamicvouchersrefundsamountpartitionedbydynamicvoucherid) | **GET** /v2/analytics/dynamicVouchers/refunds/amount/dynamicVoucher | Get refund amount of dynamic vouchers by dynamic voucher |
| [**FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticsdynamicvouchersrefundscountpartitionedbydate) | **GET** /v2/analytics/dynamicVouchers/refunds/count/date | Count refunds of dynamic vouchers by date |
| [**FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherID**](AnalyticsApi.md#fetchanalyticsdynamicvouchersrefundscountpartitionedbydynamicvoucherid) | **GET** /v2/analytics/dynamicVouchers/refunds/count/dynamicVoucher | Count refunds of dynamic vouchers by dynamic voucher |
| [**FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticshelpdeskrequestscreatedcountpartitionedbydate) | **GET** /v2/analytics/helpdeskrequests/count/date/created | Count daily help desk requests |
| [**FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticshelpdeskrequestsresolvedcountpartitionedbydate) | **GET** /v2/analytics/helpdeskrequests/count/date/resolved | Count resolved help desk requests by date |
| [**FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployee**](AnalyticsApi.md#fetchanalyticshelpdeskrequestsresolvedcountpartitionedbyemployee) | **GET** /v2/analytics/helpdeskrequests/count/employee/resolved | Count resolved help desk requests by employee |
| [**FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticshelpdeskrequestsunresolvedcountpartitionedbydate) | **GET** /v2/analytics/helpdeskrequests/count/date/unresolved | Count unresolved help desk requests by date |
| [**FetchAnalyticsItemWalletPageViews**](AnalyticsApi.md#fetchanalyticsitemwalletpageviews) | **GET** /v2/analytics/walletPageViews/item/{itemID} | Get wallet page views of item |
| [**FetchAnalyticsMemberCount**](AnalyticsApi.md#fetchanalyticsmembercount) | **GET** /v2/analytics/membership/member/count | Count members |
| [**FetchAnalyticsMerchantCreditCount**](AnalyticsApi.md#fetchanalyticsmerchantcreditcount) | **GET** /v2/analytics/membership/merchantCredit/count | Count merchant credits |
| [**FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignID**](AnalyticsApi.md#fetchanalyticsoffervsredeemedamountpartitionedbycampaignid) | **GET** /v2/analytics/campaigns/amount/campaign/offerVsRedeemed | Get offer vs redeemed amount by campaign |
| [**FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticspaymentobjectbroadcastscreatedcountpartitionedbydate) | **GET** /v2/analytics/paymentObjectBroadcasts/count/date/created | Count created broadcasts by date |
| [**FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcasts**](AnalyticsApi.md#fetchanalyticspaymentobjectbroadcastsindividualexecutiontimeofcompletedbroadcasts) | **GET** /v2/analytics/paymentObjectBroadcasts/executionTime/completed | Get execution time of completed broadcasts |
| [**FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticspaymentobjectbroadcastsscheduledcountpartitionedbydate) | **GET** /v2/analytics/paymentObjectBroadcasts/count/date/scheduled | Count scheduled broadcasts by date |
| [**FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployee**](AnalyticsApi.md#fetchanalyticspaymentobjectbroadcastsscheduledcountpartitionedbyemployee) | **GET** /v2/analytics/paymentObjectBroadcasts/count/employee/scheduled | Count scheduled broadcasts by employee |
| [**FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumber**](AnalyticsApi.md#fetchanalyticspaymentobjectbroadcastsscheduledcountpartitionedbyphonenumber) | **GET** /v2/analytics/paymentObjectBroadcasts/count/phoneNumber/scheduled | Count scheduled broadcasts by phone number |
| [**FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticspaymentobjectbroadcastsscheduledsmscountpartitionedbydate) | **GET** /v2/analytics/paymentObjectBroadcasts/sms/count/date/scheduled | Count scheduled SMS broadcasts by date |
| [**FetchAnalyticsSentOutboundMessagesCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticssentoutboundmessagescountpartitionedbydate) | **GET** /v2/analytics/outboundSMS/count/date/sent | Count sent outbound messages by date |
| [**FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumber**](AnalyticsApi.md#fetchanalyticssentoutboundmessagescountpartitionedbyphonenumber) | **GET** /v2/analytics/outboundSMS/count/phoneNumber/sent | Count sent outbound messages by phone number |
| [**FetchAnalyticsStaticVoucherWalletPageViews**](AnalyticsApi.md#fetchanalyticsstaticvoucherwalletpageviews) | **GET** /v2/analytics/walletPageViews/staticVoucher/{voucherID} | Get a static voucher&#39;s wallet page views |
| [**FetchAnalyticsTCPAFiltersCreateCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticstcpafilterscreatecountpartitionedbydate) | **GET** /v2/analytics/tcpafilters/count/date/create | Count created TCPA Filter entries by date |
| [**FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticstcpafiltersdeletecountpartitionedbydate) | **GET** /v2/analytics/tcpafilters/count/date/delete | Count deleted TCPA Filter entries by date |
| [**FetchAnalyticsTCPAStopCountPartitionedByDate**](AnalyticsApi.md#fetchanalyticstcpastopcountpartitionedbydate) | **GET** /v2/analytics/tcpa/count/date/stop | Count TCPA (STOP) entries by date |
| [**FetchAnalyticsTCPAStopCountPartitionedByPhoneNumber**](AnalyticsApi.md#fetchanalyticstcpastopcountpartitionedbyphonenumber) | **GET** /v2/analytics/tcpa/count/phoneNumber/stop | Count TCPA (STOP) entries by phone number |
| [**FetchAnalyticsTotalAmountRedeemedPerMerchantCredit**](AnalyticsApi.md#fetchanalyticstotalamountredeemedpermerchantcredit) | **GET** /v2/analytics/membership/merchantCredit/amount/redeemed | Get redeemed amount of merchant credits |
| [**FetchAnalyticsTotalAmountRedeemedPerTier**](AnalyticsApi.md#fetchanalyticstotalamountredeemedpertier) | **GET** /v2/analytics/membership/tier/amount/redeemed | Get redeemed amoun̥t of tiers |
| [**FetchAnalyticsTotalAmountRefundedPerMerchantCredit**](AnalyticsApi.md#fetchanalyticstotalamountrefundedpermerchantcredit) | **GET** /v2/analytics/membership/merchantCredit/amount/refunded | Get refunded amount of merchant credits |
| [**FetchAnalyticsTotalAmountRefundedPerTier**](AnalyticsApi.md#fetchanalyticstotalamountrefundedpertier) | **GET** /v2/analytics/membership/tier/amount/refunded | Get refunded amount of tiers |
| [**FetchAnalyticsTotalPointsRedeemed**](AnalyticsApi.md#fetchanalyticstotalpointsredeemed) | **GET** /v2/analytics/membership/member/points/redeemed | Count redeemed points |
| [**FetchAnalyticsTotalPointsRefunded**](AnalyticsApi.md#fetchanalyticstotalpointsrefunded) | **GET** /v2/analytics/membership/member/points/refunded | Count refunded points |
| [**FetchAnalyticsWalletSessionActivity**](AnalyticsApi.md#fetchanalyticswalletsessionactivity) | **GET** /v2/analytics/walletPageViews/session/activity/{sessionID} | Get session activity |
| [**FetchWalletPageViewByID**](AnalyticsApi.md#fetchwalletpageviewbyid) | **GET** /v2/analytics/walletPageViews/activity/{id} | Get session activity by wallet page view ID |
| [**ReferringSitesSummary**](AnalyticsApi.md#referringsitessummary) | **GET** /v2/analytics/walletPageViews/referringSitesSummary | Count referring sites |
| [**SumRevenue**](AnalyticsApi.md#sumrevenue) | **GET** /v2/analytics/ledger/revenue/sum | Sum ledger revenue |
| [**SumTransactions**](AnalyticsApi.md#sumtransactions) | **GET** /v2/analytics/ledger/transactions/sum | Sum ledger transaction amounts |

<a id="countallsubscribers"></a>
# **CountAllSubscribers**
> WTCountResult CountAllSubscribers (bool? isSubscribed = null, bool? isPendingAge21Verification = null, bool? isArchiveIncluded = null, DateTime? startDate = null, DateTime? endDate = null)

Count opt in list subscribers

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountAllSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var isSubscribed = true;  // bool? |  (optional) 
            var isPendingAge21Verification = true;  // bool? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count opt in list subscribers
                WTCountResult result = apiInstance.CountAllSubscribers(isSubscribed, isPendingAge21Verification, isArchiveIncluded, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountAllSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountAllSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count opt in list subscribers
    ApiResponse<WTCountResult> response = apiInstance.CountAllSubscribersWithHttpInfo(isSubscribed, isPendingAge21Verification, isArchiveIncluded, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountAllSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isSubscribed** | **bool?** |  | [optional]  |
| **isPendingAge21Verification** | **bool?** |  | [optional]  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

[**WTCountResult**](WTCountResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="countauthenticatedsessions"></a>
# **CountAuthenticatedSessions**
> Object CountAuthenticatedSessions (DateTime? startDate = null, DateTime? endDate = null)

Count authenticated sessions

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountAuthenticatedSessionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count authenticated sessions
                Object result = apiInstance.CountAuthenticatedSessions(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountAuthenticatedSessions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountAuthenticatedSessionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count authenticated sessions
    ApiResponse<Object> response = apiInstance.CountAuthenticatedSessionsWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountAuthenticatedSessionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="countdistinctredemptions"></a>
# **CountDistinctRedemptions**
> Object CountDistinctRedemptions (DateTime startDate, DateTime endDate, string? transactionType = null, string? segmentType = null)

Count distinct payment object redemptions

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountDistinctRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var transactionType = "transactionType_example";  // string? |  (optional) 
            var segmentType = "segmentType_example";  // string? |  (optional) 

            try
            {
                // Count distinct payment object redemptions
                Object result = apiInstance.CountDistinctRedemptions(startDate, endDate, transactionType, segmentType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountDistinctRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountDistinctRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count distinct payment object redemptions
    ApiResponse<Object> response = apiInstance.CountDistinctRedemptionsWithHttpInfo(startDate, endDate, transactionType, segmentType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountDistinctRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **transactionType** | **string?** |  | [optional]  |
| **segmentType** | **string?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="counthelpdeskrequests"></a>
# **CountHelpDeskRequests**
> Object CountHelpDeskRequests (DateTime startDate, DateTime endDate, string locale, string timezone, bool? isResolved = null)

Count help desk requests

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountHelpDeskRequestsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 
            var isResolved = true;  // bool? |  (optional) 

            try
            {
                // Count help desk requests
                Object result = apiInstance.CountHelpDeskRequests(startDate, endDate, locale, timezone, isResolved);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountHelpDeskRequests: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountHelpDeskRequestsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count help desk requests
    ApiResponse<Object> response = apiInstance.CountHelpDeskRequestsWithHttpInfo(startDate, endDate, locale, timezone, isResolved);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountHelpDeskRequestsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |
| **isResolved** | **bool?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="countinboundmessages"></a>
# **CountInboundMessages**
> WTCountResult CountInboundMessages (DateTime? startDate = null, DateTime? endDate = null)

Count inbound SMS messages

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountInboundMessagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count inbound SMS messages
                WTCountResult result = apiInstance.CountInboundMessages(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountInboundMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountInboundMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count inbound SMS messages
    ApiResponse<WTCountResult> response = apiInstance.CountInboundMessagesWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountInboundMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

[**WTCountResult**](WTCountResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="countnewsessions"></a>
# **CountNewSessions**
> Object CountNewSessions (DateTime? startDate = null, DateTime? endDate = null)

Count new sessions

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountNewSessionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count new sessions
                Object result = apiInstance.CountNewSessions(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountNewSessions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountNewSessionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count new sessions
    ApiResponse<Object> response = apiInstance.CountNewSessionsWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountNewSessionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="countoptinlistsubscriberspartitionedbydate"></a>
# **CountOptInListSubscribersPartitionedByDate**
> Object CountOptInListSubscribersPartitionedByDate (DateTime startDate, DateTime endDate)

Count opt in list subscribers by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountOptInListSubscribersPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count opt in list subscribers by date
                Object result = apiInstance.CountOptInListSubscribersPartitionedByDate(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountOptInListSubscribersPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountOptInListSubscribersPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count opt in list subscribers by date
    ApiResponse<Object> response = apiInstance.CountOptInListSubscribersPartitionedByDateWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountOptInListSubscribersPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="countoutboundmessages"></a>
# **CountOutboundMessages**
> WTCountResult CountOutboundMessages (DateTime? startDate = null, DateTime? endDate = null)

Count outbound SMS messages

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountOutboundMessagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count outbound SMS messages
                WTCountResult result = apiInstance.CountOutboundMessages(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountOutboundMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountOutboundMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count outbound SMS messages
    ApiResponse<WTCountResult> response = apiInstance.CountOutboundMessagesWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountOutboundMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

[**WTCountResult**](WTCountResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="counttotalsessions"></a>
# **CountTotalSessions**
> Object CountTotalSessions (DateTime? startDate = null, DateTime? endDate = null)

Count total sessions

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountTotalSessionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count total sessions
                Object result = apiInstance.CountTotalSessions(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountTotalSessions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountTotalSessionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count total sessions
    ApiResponse<Object> response = apiInstance.CountTotalSessionsWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountTotalSessionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="counttransactions"></a>
# **CountTransactions**
> Object CountTransactions (DateTime startDate, DateTime endDate, string? transactionType = null, string? segmentType = null)

Count ledger transactions

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountTransactionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var transactionType = "transactionType_example";  // string? |  (optional) 
            var segmentType = "segmentType_example";  // string? |  (optional) 

            try
            {
                // Count ledger transactions
                Object result = apiInstance.CountTransactions(startDate, endDate, transactionType, segmentType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountTransactions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountTransactionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count ledger transactions
    ApiResponse<Object> response = apiInstance.CountTransactionsWithHttpInfo(startDate, endDate, transactionType, segmentType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountTransactionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **transactionType** | **string?** |  | [optional]  |
| **segmentType** | **string?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="countverifiedwalletpageviews"></a>
# **CountVerifiedWalletPageViews**
> List&lt;WTWalletObjectPrefixCounts&gt; CountVerifiedWalletPageViews (DateTime startDate, DateTime endDate)

Get wallet object counts within a given time frame that have a valid phone verification token

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountVerifiedWalletPageViewsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get wallet object counts within a given time frame that have a valid phone verification token
                List<WTWalletObjectPrefixCounts> result = apiInstance.CountVerifiedWalletPageViews(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountVerifiedWalletPageViews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountVerifiedWalletPageViewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get wallet object counts within a given time frame that have a valid phone verification token
    ApiResponse<List<WTWalletObjectPrefixCounts>> response = apiInstance.CountVerifiedWalletPageViewsWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountVerifiedWalletPageViewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

[**List&lt;WTWalletObjectPrefixCounts&gt;**](WTWalletObjectPrefixCounts.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="countwalletpageviews"></a>
# **CountWalletPageViews**
> List&lt;WTWalletObjectPrefixCounts&gt; CountWalletPageViews (DateTime startDate, DateTime endDate)

Get wallet object counts within a given time frame

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class CountWalletPageViewsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get wallet object counts within a given time frame
                List<WTWalletObjectPrefixCounts> result = apiInstance.CountWalletPageViews(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.CountWalletPageViews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountWalletPageViewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get wallet object counts within a given time frame
    ApiResponse<List<WTWalletObjectPrefixCounts>> response = apiInstance.CountWalletPageViewsWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.CountWalletPageViewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

[**List&lt;WTWalletObjectPrefixCounts&gt;**](WTWalletObjectPrefixCounts.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="exitlinksummary"></a>
# **ExitLinkSummary**
> Object ExitLinkSummary (DateTime? startDate = null, DateTime? endDate = null)

Count exit clicks

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class ExitLinkSummaryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count exit clicks
                Object result = apiInstance.ExitLinkSummary(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.ExitLinkSummary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExitLinkSummaryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count exit clicks
    ApiResponse<Object> response = apiInstance.ExitLinkSummaryWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.ExitLinkSummaryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditscountpartitionedbyemployee"></a>
# **FetchAnalyticsAdCreditsCountPartitionedByEmployee**
> List&lt;Object&gt; FetchAnalyticsAdCreditsCountPartitionedByEmployee (DateTime startDate, DateTime endDate)

Count ad credits by employee

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsCountPartitionedByEmployeeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count ad credits by employee
                List<Object> result = apiInstance.FetchAnalyticsAdCreditsCountPartitionedByEmployee(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsCountPartitionedByEmployee: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsCountPartitionedByEmployeeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count ad credits by employee
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsAdCreditsCountPartitionedByEmployeeWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsCountPartitionedByEmployeeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditscountpartitionedbypaymentdesign"></a>
# **FetchAnalyticsAdCreditsCountPartitionedByPaymentDesign**
> List&lt;Object&gt; FetchAnalyticsAdCreditsCountPartitionedByPaymentDesign (DateTime startDate, DateTime endDate)

Count ad credits by payment design

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsCountPartitionedByPaymentDesignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count ad credits by payment design
                List<Object> result = apiInstance.FetchAnalyticsAdCreditsCountPartitionedByPaymentDesign(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsCountPartitionedByPaymentDesign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsCountPartitionedByPaymentDesignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count ad credits by payment design
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsAdCreditsCountPartitionedByPaymentDesignWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsCountPartitionedByPaymentDesignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditscountpartitionedbyvaluetype"></a>
# **FetchAnalyticsAdCreditsCountPartitionedByValueType**
> Object FetchAnalyticsAdCreditsCountPartitionedByValueType (DateTime startDate, DateTime endDate)

Count ad credits by value type

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsCountPartitionedByValueTypeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count ad credits by value type
                Object result = apiInstance.FetchAnalyticsAdCreditsCountPartitionedByValueType(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsCountPartitionedByValueType: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsCountPartitionedByValueTypeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count ad credits by value type
    ApiResponse<Object> response = apiInstance.FetchAnalyticsAdCreditsCountPartitionedByValueTypeWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsCountPartitionedByValueTypeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsredemptionsamountpartitionedbyadcreditid"></a>
# **FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditID**
> List&lt;Object&gt; FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditID (DateTime startDate, DateTime endDate)

Get redemption amount of ad credits by Ad Credit

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get redemption amount of ad credits by Ad Credit
                List<Object> result = apiInstance.FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redemption amount of ad credits by Ad Credit
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByAdCreditIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsredemptionsamountpartitionedbydate"></a>
# **FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDate**
> Object FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Get redemption amount of ad credits by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get redemption amount of ad credits by date
                Object result = apiInstance.FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redemption amount of ad credits by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRedemptionsAmountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsredemptionscountpartitionedbyadcreditid"></a>
# **FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditID**
> List&lt;Object&gt; FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditID (DateTime startDate, DateTime endDate)

Count redemptions of ad credits by Ad Credit

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count redemptions of ad credits by Ad Credit
                List<Object> result = apiInstance.FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redemptions of ad credits by Ad Credit
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRedemptionsCountPartitionedByAdCreditIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsredemptionscountpartitionedbydate"></a>
# **FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDate**
> Object FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count redemptions of ad credits by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count redemptions of ad credits by date
                Object result = apiInstance.FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redemptions of ad credits by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRedemptionsCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsrefundsamountpartitionedbyadcreditid"></a>
# **FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditID**
> List&lt;Object&gt; FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditID (DateTime startDate, DateTime endDate)

Get refund amount of ad credits by Ad Credit

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get refund amount of ad credits by Ad Credit
                List<Object> result = apiInstance.FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refund amount of ad credits by Ad Credit
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRefundsAmountPartitionedByAdCreditIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsrefundsamountpartitionedbydate"></a>
# **FetchAnalyticsAdCreditsRefundsAmountPartitionedByDate**
> Object FetchAnalyticsAdCreditsRefundsAmountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Get refund amount of ad credits by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsRefundsAmountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get refund amount of ad credits by date
                Object result = apiInstance.FetchAnalyticsAdCreditsRefundsAmountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRefundsAmountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsRefundsAmountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refund amount of ad credits by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsAdCreditsRefundsAmountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRefundsAmountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsrefundscountpartitionedbyadcreditid"></a>
# **FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditID**
> List&lt;Object&gt; FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditID (DateTime startDate, DateTime endDate)

Count refunds of ad credits by Ad Credit

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count refunds of ad credits by Ad Credit
                List<Object> result = apiInstance.FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunds of ad credits by Ad Credit
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRefundsCountPartitionedByAdCreditIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsrefundscountpartitionedbydate"></a>
# **FetchAnalyticsAdCreditsRefundsCountPartitionedByDate**
> Object FetchAnalyticsAdCreditsRefundsCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count refunds of ad credits by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsRefundsCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count refunds of ad credits by date
                Object result = apiInstance.FetchAnalyticsAdCreditsRefundsCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRefundsCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsRefundsCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunds of ad credits by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsAdCreditsRefundsCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsRefundsCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsscanscountpartitionedbyadcreditid"></a>
# **FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditID**
> List&lt;Object&gt; FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditID (DateTime startDate, DateTime endDate)

Count scans of ad credits by Ad Credit

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count scans of ad credits by Ad Credit
                List<Object> result = apiInstance.FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count scans of ad credits by Ad Credit
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsScansCountPartitionedByAdCreditIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsadcreditsscanscountpartitionedbydate"></a>
# **FetchAnalyticsAdCreditsScansCountPartitionedByDate**
> Object FetchAnalyticsAdCreditsScansCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count scans of ad credits by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsAdCreditsScansCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count scans of ad credits by date
                Object result = apiInstance.FetchAnalyticsAdCreditsScansCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsScansCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsAdCreditsScansCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count scans of ad credits by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsAdCreditsScansCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsAdCreditsScansCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignwalletpageviews"></a>
# **FetchAnalyticsCampaignWalletPageViews**
> List&lt;WTWalletPageView&gt; FetchAnalyticsCampaignWalletPageViews (string campaignID)

Get a campaign's wallet page views

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignWalletPageViewsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Get a campaign's wallet page views
                List<WTWalletPageView> result = apiInstance.FetchAnalyticsCampaignWalletPageViews(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignWalletPageViews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignWalletPageViewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a campaign's wallet page views
    ApiResponse<List<WTWalletPageView>> response = apiInstance.FetchAnalyticsCampaignWalletPageViewsWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignWalletPageViewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**List&lt;WTWalletPageView&gt;**](WTWalletPageView.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignscountpartitionedbycampaignid"></a>
# **FetchAnalyticsCampaignsCountPartitionedByCampaignID**
> List&lt;Object&gt; FetchAnalyticsCampaignsCountPartitionedByCampaignID (DateTime startDate, DateTime endDate)

Count created campaigns by campaign

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsCountPartitionedByCampaignIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count created campaigns by campaign
                List<Object> result = apiInstance.FetchAnalyticsCampaignsCountPartitionedByCampaignID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsCountPartitionedByCampaignID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsCountPartitionedByCampaignIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count created campaigns by campaign
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsCampaignsCountPartitionedByCampaignIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsCountPartitionedByCampaignIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignscountpartitionedbyemployee"></a>
# **FetchAnalyticsCampaignsCountPartitionedByEmployee**
> List&lt;Object&gt; FetchAnalyticsCampaignsCountPartitionedByEmployee (DateTime startDate, DateTime endDate)

Count campaigns by employee

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsCountPartitionedByEmployeeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count campaigns by employee
                List<Object> result = apiInstance.FetchAnalyticsCampaignsCountPartitionedByEmployee(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsCountPartitionedByEmployee: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsCountPartitionedByEmployeeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count campaigns by employee
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsCampaignsCountPartitionedByEmployeeWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsCountPartitionedByEmployeeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignscountpartitionedbypaymentdesign"></a>
# **FetchAnalyticsCampaignsCountPartitionedByPaymentDesign**
> List&lt;Object&gt; FetchAnalyticsCampaignsCountPartitionedByPaymentDesign (DateTime startDate, DateTime endDate)

Count campaigns by payment design

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsCountPartitionedByPaymentDesignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count campaigns by payment design
                List<Object> result = apiInstance.FetchAnalyticsCampaignsCountPartitionedByPaymentDesign(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsCountPartitionedByPaymentDesign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsCountPartitionedByPaymentDesignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count campaigns by payment design
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsCampaignsCountPartitionedByPaymentDesignWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsCountPartitionedByPaymentDesignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignscountpartitionedbyvaluetype"></a>
# **FetchAnalyticsCampaignsCountPartitionedByValueType**
> Object FetchAnalyticsCampaignsCountPartitionedByValueType (DateTime startDate, DateTime endDate)

Count campaigns by value type

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsCountPartitionedByValueTypeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count campaigns by value type
                Object result = apiInstance.FetchAnalyticsCampaignsCountPartitionedByValueType(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsCountPartitionedByValueType: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsCountPartitionedByValueTypeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count campaigns by value type
    ApiResponse<Object> response = apiInstance.FetchAnalyticsCampaignsCountPartitionedByValueTypeWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsCountPartitionedByValueTypeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignsredemptionsamountpartitionedbycampaignid"></a>
# **FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignID**
> List&lt;Object&gt; FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignID (DateTime startDate, DateTime endDate)

Get redemption amount of campaigns by Campaign

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get redemption amount of campaigns by Campaign
                List<Object> result = apiInstance.FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redemption amount of campaigns by Campaign
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRedemptionsAmountPartitionedByCampaignIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignsredemptionsamountpartitionedbydate"></a>
# **FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDate**
> Object FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Get redemption amount of campaigns by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get redemption amount of campaigns by date
                Object result = apiInstance.FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redemption amount of campaigns by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRedemptionsAmountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignsredemptionscountpartitionedbycampaignid"></a>
# **FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignID**
> List&lt;Object&gt; FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignID (DateTime startDate, DateTime endDate)

Count redemptions of campaigns by Campaign

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count redemptions of campaigns by Campaign
                List<Object> result = apiInstance.FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redemptions of campaigns by Campaign
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRedemptionsCountPartitionedByCampaignIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignsredemptionscountpartitionedbydate"></a>
# **FetchAnalyticsCampaignsRedemptionsCountPartitionedByDate**
> Object FetchAnalyticsCampaignsRedemptionsCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count redemptions of campaigns by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsRedemptionsCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count redemptions of campaigns by date
                Object result = apiInstance.FetchAnalyticsCampaignsRedemptionsCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRedemptionsCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsRedemptionsCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redemptions of campaigns by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsCampaignsRedemptionsCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRedemptionsCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignsrefundsamountpartitionedbycampaignid"></a>
# **FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignID**
> List&lt;Object&gt; FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignID (DateTime startDate, DateTime endDate)

Get refund amount of campaigns by Campaign

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get refund amount of campaigns by Campaign
                List<Object> result = apiInstance.FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refund amount of campaigns by Campaign
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRefundsAmountPartitionedByCampaignIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignsrefundsamountpartitionedbydate"></a>
# **FetchAnalyticsCampaignsRefundsAmountPartitionedByDate**
> Object FetchAnalyticsCampaignsRefundsAmountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Get refund amount of campaigns by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsRefundsAmountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get refund amount of campaigns by date
                Object result = apiInstance.FetchAnalyticsCampaignsRefundsAmountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRefundsAmountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsRefundsAmountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refund amount of campaigns by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsCampaignsRefundsAmountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRefundsAmountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignsrefundscountpartitionedbycampaignid"></a>
# **FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignID**
> List&lt;Object&gt; FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignID (DateTime startDate, DateTime endDate)

Count refunds of campaigns by Campaign

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count refunds of campaigns by Campaign
                List<Object> result = apiInstance.FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunds of campaigns by Campaign
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRefundsCountPartitionedByCampaignIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticscampaignsrefundscountpartitionedbydate"></a>
# **FetchAnalyticsCampaignsRefundsCountPartitionedByDate**
> Object FetchAnalyticsCampaignsRefundsCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count refunds of campaigns by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsCampaignsRefundsCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count refunds of campaigns by date
                Object result = apiInstance.FetchAnalyticsCampaignsRefundsCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRefundsCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsCampaignsRefundsCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunds of campaigns by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsCampaignsRefundsCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsCampaignsRefundsCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdeliveredoutboundmessagescountpartitionedbydate"></a>
# **FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDate**
> Object FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count delivered outbound messages by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count delivered outbound messages by date
                Object result = apiInstance.FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count delivered outbound messages by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdeliveredoutboundmessagescountpartitionedbyphonenumber"></a>
# **FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumber**
> List&lt;Object&gt; FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumber (DateTime startDate, DateTime endDate)

Count delivered outbound messages by phone number

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count delivered outbound messages by phone number
                List<Object> result = apiInstance.FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumber(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count delivered outbound messages by phone number
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumberWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDeliveredOutboundMessagesCountPartitionedByPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdistinctwalletsessions"></a>
# **FetchAnalyticsDistinctWalletSessions**
> Object FetchAnalyticsDistinctWalletSessions (DateTime? startDate = null, DateTime? endDate = null)

Get distinct wallet sessions

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDistinctWalletSessionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get distinct wallet sessions
                Object result = apiInstance.FetchAnalyticsDistinctWalletSessions(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDistinctWalletSessions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDistinctWalletSessionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get distinct wallet sessions
    ApiResponse<Object> response = apiInstance.FetchAnalyticsDistinctWalletSessionsWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDistinctWalletSessionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvoucherscountpartitionedbyemployee"></a>
# **FetchAnalyticsDynamicVouchersCountPartitionedByEmployee**
> List&lt;Object&gt; FetchAnalyticsDynamicVouchersCountPartitionedByEmployee (DateTime startDate, DateTime endDate)

Count dynamic vouchers by employee

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersCountPartitionedByEmployeeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count dynamic vouchers by employee
                List<Object> result = apiInstance.FetchAnalyticsDynamicVouchersCountPartitionedByEmployee(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersCountPartitionedByEmployee: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersCountPartitionedByEmployeeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count dynamic vouchers by employee
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsDynamicVouchersCountPartitionedByEmployeeWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersCountPartitionedByEmployeeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvoucherscountpartitionedbypaymentdesign"></a>
# **FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesign**
> List&lt;Object&gt; FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesign (DateTime startDate, DateTime endDate)

Count dynamic vouchers by payment design

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count dynamic vouchers by payment design
                List<Object> result = apiInstance.FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesign(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count dynamic vouchers by payment design
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesignWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersCountPartitionedByPaymentDesignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvouchersredemptionsamountpartitionedbydate"></a>
# **FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDate**
> Object FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Get redemption amount of dynamic vouchers by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get redemption amount of dynamic vouchers by date
                Object result = apiInstance.FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redemption amount of dynamic vouchers by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvouchersredemptionsamountpartitionedbydynamicvoucherid"></a>
# **FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherID**
> List&lt;Object&gt; FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherID (DateTime startDate, DateTime endDate)

Get redemption amount of dynamic vouchers by dynamic voucher

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get redemption amount of dynamic vouchers by dynamic voucher
                List<Object> result = apiInstance.FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redemption amount of dynamic vouchers by dynamic voucher
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRedemptionsAmountPartitionedByDynamicVoucherIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvouchersredemptionscountpartitionedbydate"></a>
# **FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDate**
> List&lt;Object&gt; FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count redemptions of dynamic vouchers by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count redemptions of dynamic vouchers by date
                List<Object> result = apiInstance.FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redemptions of dynamic vouchers by date
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvouchersredemptionscountpartitionedbydynamicvoucherid"></a>
# **FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherID**
> List&lt;Object&gt; FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherID (DateTime startDate, DateTime endDate)

Count redemptions of dynamic vouchers by dynamic voucher

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count redemptions of dynamic vouchers by dynamic voucher
                List<Object> result = apiInstance.FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redemptions of dynamic vouchers by dynamic voucher
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRedemptionsCountPartitionedByDynamicVoucherIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvouchersrefundsamountpartitionedbydate"></a>
# **FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDate**
> Object FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Get refund amount of dynamic vouchers by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get refund amount of dynamic vouchers by date
                Object result = apiInstance.FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refund amount of dynamic vouchers by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvouchersrefundsamountpartitionedbydynamicvoucherid"></a>
# **FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherID**
> List&lt;Object&gt; FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherID (DateTime startDate, DateTime endDate)

Get refund amount of dynamic vouchers by dynamic voucher

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get refund amount of dynamic vouchers by dynamic voucher
                List<Object> result = apiInstance.FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refund amount of dynamic vouchers by dynamic voucher
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRefundsAmountPartitionedByDynamicVoucherIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvouchersrefundscountpartitionedbydate"></a>
# **FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDate**
> Object FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count refunds of dynamic vouchers by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count refunds of dynamic vouchers by date
                Object result = apiInstance.FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunds of dynamic vouchers by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsdynamicvouchersrefundscountpartitionedbydynamicvoucherid"></a>
# **FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherID**
> List&lt;Object&gt; FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherID (DateTime startDate, DateTime endDate)

Count refunds of dynamic vouchers by dynamic voucher

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count refunds of dynamic vouchers by dynamic voucher
                List<Object> result = apiInstance.FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunds of dynamic vouchers by dynamic voucher
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsDynamicVouchersRefundsCountPartitionedByDynamicVoucherIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticshelpdeskrequestscreatedcountpartitionedbydate"></a>
# **FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDate**
> Object FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count daily help desk requests

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count daily help desk requests
                Object result = apiInstance.FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count daily help desk requests
    ApiResponse<Object> response = apiInstance.FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsHelpDeskRequestsCreatedCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticshelpdeskrequestsresolvedcountpartitionedbydate"></a>
# **FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDate**
> Object FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count resolved help desk requests by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count resolved help desk requests by date
                Object result = apiInstance.FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count resolved help desk requests by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticshelpdeskrequestsresolvedcountpartitionedbyemployee"></a>
# **FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployee**
> List&lt;Object&gt; FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployee (DateTime startDate, DateTime endDate)

Count resolved help desk requests by employee

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployeeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count resolved help desk requests by employee
                List<Object> result = apiInstance.FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployee(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployee: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployeeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count resolved help desk requests by employee
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployeeWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsHelpDeskRequestsResolvedCountPartitionedByEmployeeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticshelpdeskrequestsunresolvedcountpartitionedbydate"></a>
# **FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDate**
> Object FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count unresolved help desk requests by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count unresolved help desk requests by date
                Object result = apiInstance.FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count unresolved help desk requests by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsHelpDeskRequestsUnresolvedCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsitemwalletpageviews"></a>
# **FetchAnalyticsItemWalletPageViews**
> Object FetchAnalyticsItemWalletPageViews (string itemID)

Get wallet page views of item

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsItemWalletPageViewsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 

            try
            {
                // Get wallet page views of item
                Object result = apiInstance.FetchAnalyticsItemWalletPageViews(itemID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsItemWalletPageViews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsItemWalletPageViewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get wallet page views of item
    ApiResponse<Object> response = apiInstance.FetchAnalyticsItemWalletPageViewsWithHttpInfo(itemID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsItemWalletPageViewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemID** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsmembercount"></a>
# **FetchAnalyticsMemberCount**
> List&lt;MSAnalyticsMemberCountPartitionedByDate&gt; FetchAnalyticsMemberCount (DateTime startDate, DateTime endDate, string locale, string timezone)

Count members

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsMemberCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count members
                List<MSAnalyticsMemberCountPartitionedByDate> result = apiInstance.FetchAnalyticsMemberCount(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsMemberCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsMemberCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count members
    ApiResponse<List<MSAnalyticsMemberCountPartitionedByDate>> response = apiInstance.FetchAnalyticsMemberCountWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsMemberCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

[**List&lt;MSAnalyticsMemberCountPartitionedByDate&gt;**](MSAnalyticsMemberCountPartitionedByDate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsmerchantcreditcount"></a>
# **FetchAnalyticsMerchantCreditCount**
> Object FetchAnalyticsMerchantCreditCount (DateTime startDate, DateTime endDate, string locale, string timezone)

Count merchant credits

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsMerchantCreditCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count merchant credits
                Object result = apiInstance.FetchAnalyticsMerchantCreditCount(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsMerchantCreditCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsMerchantCreditCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count merchant credits
    ApiResponse<Object> response = apiInstance.FetchAnalyticsMerchantCreditCountWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsMerchantCreditCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsoffervsredeemedamountpartitionedbycampaignid"></a>
# **FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignID**
> List&lt;Object&gt; FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignID (DateTime startDate, DateTime endDate)

Get offer vs redeemed amount by campaign

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get offer vs redeemed amount by campaign
                List<Object> result = apiInstance.FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignID(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get offer vs redeemed amount by campaign
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignIDWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsOfferVsRedeemedAmountPartitionedByCampaignIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticspaymentobjectbroadcastscreatedcountpartitionedbydate"></a>
# **FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDate**
> Object FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count created broadcasts by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count created broadcasts by date
                Object result = apiInstance.FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count created broadcasts by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsCreatedCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticspaymentobjectbroadcastsindividualexecutiontimeofcompletedbroadcasts"></a>
# **FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcasts**
> Object FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcasts (DateTime startDate, DateTime endDate)

Get execution time of completed broadcasts

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcastsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get execution time of completed broadcasts
                Object result = apiInstance.FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcasts(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcasts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcastsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get execution time of completed broadcasts
    ApiResponse<Object> response = apiInstance.FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcastsWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsIndividualExecutionTimeOfCompletedBroadcastsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticspaymentobjectbroadcastsscheduledcountpartitionedbydate"></a>
# **FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDate**
> Object FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count scheduled broadcasts by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count scheduled broadcasts by date
                Object result = apiInstance.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count scheduled broadcasts by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticspaymentobjectbroadcastsscheduledcountpartitionedbyemployee"></a>
# **FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployee**
> List&lt;Object&gt; FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployee (DateTime startDate, DateTime endDate)

Count scheduled broadcasts by employee

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployeeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count scheduled broadcasts by employee
                List<Object> result = apiInstance.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployee(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployee: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployeeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count scheduled broadcasts by employee
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployeeWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByEmployeeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticspaymentobjectbroadcastsscheduledcountpartitionedbyphonenumber"></a>
# **FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumber**
> List&lt;Object&gt; FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumber (DateTime startDate, DateTime endDate)

Count scheduled broadcasts by phone number

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count scheduled broadcasts by phone number
                List<Object> result = apiInstance.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumber(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count scheduled broadcasts by phone number
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumberWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsScheduledCountPartitionedByPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticspaymentobjectbroadcastsscheduledsmscountpartitionedbydate"></a>
# **FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDate**
> Object FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count scheduled SMS broadcasts by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count scheduled SMS broadcasts by date
                Object result = apiInstance.FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count scheduled SMS broadcasts by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsPaymentObjectBroadcastsScheduledSMSCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticssentoutboundmessagescountpartitionedbydate"></a>
# **FetchAnalyticsSentOutboundMessagesCountPartitionedByDate**
> Object FetchAnalyticsSentOutboundMessagesCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count sent outbound messages by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsSentOutboundMessagesCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count sent outbound messages by date
                Object result = apiInstance.FetchAnalyticsSentOutboundMessagesCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsSentOutboundMessagesCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsSentOutboundMessagesCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count sent outbound messages by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsSentOutboundMessagesCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsSentOutboundMessagesCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticssentoutboundmessagescountpartitionedbyphonenumber"></a>
# **FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumber**
> List&lt;Object&gt; FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumber (DateTime startDate, DateTime endDate)

Count sent outbound messages by phone number

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count sent outbound messages by phone number
                List<Object> result = apiInstance.FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumber(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count sent outbound messages by phone number
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumberWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsSentOutboundMessagesCountPartitionedByPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticsstaticvoucherwalletpageviews"></a>
# **FetchAnalyticsStaticVoucherWalletPageViews**
> List&lt;WTWalletPageView&gt; FetchAnalyticsStaticVoucherWalletPageViews (string voucherID)

Get a static voucher's wallet page views

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsStaticVoucherWalletPageViewsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var voucherID = "voucherID_example";  // string | 

            try
            {
                // Get a static voucher's wallet page views
                List<WTWalletPageView> result = apiInstance.FetchAnalyticsStaticVoucherWalletPageViews(voucherID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsStaticVoucherWalletPageViews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsStaticVoucherWalletPageViewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a static voucher's wallet page views
    ApiResponse<List<WTWalletPageView>> response = apiInstance.FetchAnalyticsStaticVoucherWalletPageViewsWithHttpInfo(voucherID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsStaticVoucherWalletPageViewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **voucherID** | **string** |  |  |

### Return type

[**List&lt;WTWalletPageView&gt;**](WTWalletPageView.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstcpafilterscreatecountpartitionedbydate"></a>
# **FetchAnalyticsTCPAFiltersCreateCountPartitionedByDate**
> Object FetchAnalyticsTCPAFiltersCreateCountPartitionedByDate (DateTime startDate, DateTime endDate)

Count created TCPA Filter entries by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTCPAFiltersCreateCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count created TCPA Filter entries by date
                Object result = apiInstance.FetchAnalyticsTCPAFiltersCreateCountPartitionedByDate(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTCPAFiltersCreateCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTCPAFiltersCreateCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count created TCPA Filter entries by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsTCPAFiltersCreateCountPartitionedByDateWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTCPAFiltersCreateCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstcpafiltersdeletecountpartitionedbydate"></a>
# **FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDate**
> Object FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDate (DateTime startDate, DateTime endDate)

Count deleted TCPA Filter entries by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count deleted TCPA Filter entries by date
                Object result = apiInstance.FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDate(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count deleted TCPA Filter entries by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDateWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTCPAFiltersDeleteCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstcpastopcountpartitionedbydate"></a>
# **FetchAnalyticsTCPAStopCountPartitionedByDate**
> Object FetchAnalyticsTCPAStopCountPartitionedByDate (DateTime startDate, DateTime endDate, string locale, string timezone)

Count TCPA (STOP) entries by date

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTCPAStopCountPartitionedByDateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count TCPA (STOP) entries by date
                Object result = apiInstance.FetchAnalyticsTCPAStopCountPartitionedByDate(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTCPAStopCountPartitionedByDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTCPAStopCountPartitionedByDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count TCPA (STOP) entries by date
    ApiResponse<Object> response = apiInstance.FetchAnalyticsTCPAStopCountPartitionedByDateWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTCPAStopCountPartitionedByDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstcpastopcountpartitionedbyphonenumber"></a>
# **FetchAnalyticsTCPAStopCountPartitionedByPhoneNumber**
> List&lt;Object&gt; FetchAnalyticsTCPAStopCountPartitionedByPhoneNumber (DateTime startDate, DateTime endDate)

Count TCPA (STOP) entries by phone number

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTCPAStopCountPartitionedByPhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count TCPA (STOP) entries by phone number
                List<Object> result = apiInstance.FetchAnalyticsTCPAStopCountPartitionedByPhoneNumber(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTCPAStopCountPartitionedByPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTCPAStopCountPartitionedByPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count TCPA (STOP) entries by phone number
    ApiResponse<List<Object>> response = apiInstance.FetchAnalyticsTCPAStopCountPartitionedByPhoneNumberWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTCPAStopCountPartitionedByPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstotalamountredeemedpermerchantcredit"></a>
# **FetchAnalyticsTotalAmountRedeemedPerMerchantCredit**
> Object FetchAnalyticsTotalAmountRedeemedPerMerchantCredit (DateTime startDate, DateTime endDate, string locale, string timezone)

Get redeemed amount of merchant credits

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTotalAmountRedeemedPerMerchantCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get redeemed amount of merchant credits
                Object result = apiInstance.FetchAnalyticsTotalAmountRedeemedPerMerchantCredit(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalAmountRedeemedPerMerchantCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTotalAmountRedeemedPerMerchantCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redeemed amount of merchant credits
    ApiResponse<Object> response = apiInstance.FetchAnalyticsTotalAmountRedeemedPerMerchantCreditWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalAmountRedeemedPerMerchantCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstotalamountredeemedpertier"></a>
# **FetchAnalyticsTotalAmountRedeemedPerTier**
> List&lt;MSAnalyticsMembershipTierAmountRedeemedPartitionedByDate&gt; FetchAnalyticsTotalAmountRedeemedPerTier (DateTime startDate, DateTime endDate, string locale, string timezone)

Get redeemed amoun̥t of tiers

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTotalAmountRedeemedPerTierExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get redeemed amoun̥t of tiers
                List<MSAnalyticsMembershipTierAmountRedeemedPartitionedByDate> result = apiInstance.FetchAnalyticsTotalAmountRedeemedPerTier(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalAmountRedeemedPerTier: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTotalAmountRedeemedPerTierWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redeemed amoun̥t of tiers
    ApiResponse<List<MSAnalyticsMembershipTierAmountRedeemedPartitionedByDate>> response = apiInstance.FetchAnalyticsTotalAmountRedeemedPerTierWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalAmountRedeemedPerTierWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

[**List&lt;MSAnalyticsMembershipTierAmountRedeemedPartitionedByDate&gt;**](MSAnalyticsMembershipTierAmountRedeemedPartitionedByDate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstotalamountrefundedpermerchantcredit"></a>
# **FetchAnalyticsTotalAmountRefundedPerMerchantCredit**
> Object FetchAnalyticsTotalAmountRefundedPerMerchantCredit (DateTime startDate, DateTime endDate, string locale, string timezone)

Get refunded amount of merchant credits

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTotalAmountRefundedPerMerchantCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get refunded amount of merchant credits
                Object result = apiInstance.FetchAnalyticsTotalAmountRefundedPerMerchantCredit(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalAmountRefundedPerMerchantCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTotalAmountRefundedPerMerchantCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refunded amount of merchant credits
    ApiResponse<Object> response = apiInstance.FetchAnalyticsTotalAmountRefundedPerMerchantCreditWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalAmountRefundedPerMerchantCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstotalamountrefundedpertier"></a>
# **FetchAnalyticsTotalAmountRefundedPerTier**
> List&lt;MSAnalyticsMembershipTierAmountRefundedPartitionedByDate&gt; FetchAnalyticsTotalAmountRefundedPerTier (DateTime startDate, DateTime endDate, string locale, string timezone)

Get refunded amount of tiers

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTotalAmountRefundedPerTierExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Get refunded amount of tiers
                List<MSAnalyticsMembershipTierAmountRefundedPartitionedByDate> result = apiInstance.FetchAnalyticsTotalAmountRefundedPerTier(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalAmountRefundedPerTier: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTotalAmountRefundedPerTierWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refunded amount of tiers
    ApiResponse<List<MSAnalyticsMembershipTierAmountRefundedPartitionedByDate>> response = apiInstance.FetchAnalyticsTotalAmountRefundedPerTierWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalAmountRefundedPerTierWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

[**List&lt;MSAnalyticsMembershipTierAmountRefundedPartitionedByDate&gt;**](MSAnalyticsMembershipTierAmountRefundedPartitionedByDate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstotalpointsredeemed"></a>
# **FetchAnalyticsTotalPointsRedeemed**
> List&lt;MSAnalyticsMemberPointsRedeemedPartitionedByDate&gt; FetchAnalyticsTotalPointsRedeemed (DateTime startDate, DateTime endDate, string locale, string timezone)

Count redeemed points

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTotalPointsRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count redeemed points
                List<MSAnalyticsMemberPointsRedeemedPartitionedByDate> result = apiInstance.FetchAnalyticsTotalPointsRedeemed(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalPointsRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTotalPointsRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redeemed points
    ApiResponse<List<MSAnalyticsMemberPointsRedeemedPartitionedByDate>> response = apiInstance.FetchAnalyticsTotalPointsRedeemedWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalPointsRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

[**List&lt;MSAnalyticsMemberPointsRedeemedPartitionedByDate&gt;**](MSAnalyticsMemberPointsRedeemedPartitionedByDate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticstotalpointsrefunded"></a>
# **FetchAnalyticsTotalPointsRefunded**
> List&lt;MSAnalyticsMemberPointsRefundedPartitionedByDate&gt; FetchAnalyticsTotalPointsRefunded (DateTime startDate, DateTime endDate, string locale, string timezone)

Count refunded points

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsTotalPointsRefundedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var locale = "locale_example";  // string | 
            var timezone = "timezone_example";  // string | 

            try
            {
                // Count refunded points
                List<MSAnalyticsMemberPointsRefundedPartitionedByDate> result = apiInstance.FetchAnalyticsTotalPointsRefunded(startDate, endDate, locale, timezone);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalPointsRefunded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsTotalPointsRefundedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunded points
    ApiResponse<List<MSAnalyticsMemberPointsRefundedPartitionedByDate>> response = apiInstance.FetchAnalyticsTotalPointsRefundedWithHttpInfo(startDate, endDate, locale, timezone);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsTotalPointsRefundedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **locale** | **string** |  |  |
| **timezone** | **string** |  |  |

### Return type

[**List&lt;MSAnalyticsMemberPointsRefundedPartitionedByDate&gt;**](MSAnalyticsMemberPointsRefundedPartitionedByDate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchanalyticswalletsessionactivity"></a>
# **FetchAnalyticsWalletSessionActivity**
> List&lt;WTWalletPageView&gt; FetchAnalyticsWalletSessionActivity (string sessionID)

Get session activity

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchAnalyticsWalletSessionActivityExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var sessionID = "sessionID_example";  // string | 

            try
            {
                // Get session activity
                List<WTWalletPageView> result = apiInstance.FetchAnalyticsWalletSessionActivity(sessionID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsWalletSessionActivity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAnalyticsWalletSessionActivityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get session activity
    ApiResponse<List<WTWalletPageView>> response = apiInstance.FetchAnalyticsWalletSessionActivityWithHttpInfo(sessionID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchAnalyticsWalletSessionActivityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sessionID** | **string** |  |  |

### Return type

[**List&lt;WTWalletPageView&gt;**](WTWalletPageView.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchwalletpageviewbyid"></a>
# **FetchWalletPageViewByID**
> WalletPageView FetchWalletPageViewByID (string id)

Get session activity by wallet page view ID

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class FetchWalletPageViewByIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get session activity by wallet page view ID
                WalletPageView result = apiInstance.FetchWalletPageViewByID(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.FetchWalletPageViewByID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletPageViewByIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get session activity by wallet page view ID
    ApiResponse<WalletPageView> response = apiInstance.FetchWalletPageViewByIDWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.FetchWalletPageViewByIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WalletPageView**](WalletPageView.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="referringsitessummary"></a>
# **ReferringSitesSummary**
> Object ReferringSitesSummary (DateTime? startDate = null, DateTime? endDate = null)

Count referring sites

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class ReferringSitesSummaryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count referring sites
                Object result = apiInstance.ReferringSitesSummary(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.ReferringSitesSummary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReferringSitesSummaryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count referring sites
    ApiResponse<Object> response = apiInstance.ReferringSitesSummaryWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.ReferringSitesSummaryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sumrevenue"></a>
# **SumRevenue**
> Object SumRevenue (DateTime startDate, DateTime endDate, string? transactionType = null, string? segmentType = null)

Sum ledger revenue

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class SumRevenueExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var transactionType = "transactionType_example";  // string? |  (optional) 
            var segmentType = "segmentType_example";  // string? |  (optional) 

            try
            {
                // Sum ledger revenue
                Object result = apiInstance.SumRevenue(startDate, endDate, transactionType, segmentType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.SumRevenue: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SumRevenueWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sum ledger revenue
    ApiResponse<Object> response = apiInstance.SumRevenueWithHttpInfo(startDate, endDate, transactionType, segmentType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.SumRevenueWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **transactionType** | **string?** |  | [optional]  |
| **segmentType** | **string?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sumtransactions"></a>
# **SumTransactions**
> Object SumTransactions (DateTime startDate, DateTime endDate, string? transactionType = null, string? segmentType = null)

Sum ledger transaction amounts

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

namespace Example
{
    public class SumTransactionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AnalyticsApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var transactionType = "transactionType_example";  // string? |  (optional) 
            var segmentType = "segmentType_example";  // string? |  (optional) 

            try
            {
                // Sum ledger transaction amounts
                Object result = apiInstance.SumTransactions(startDate, endDate, transactionType, segmentType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsApi.SumTransactions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SumTransactionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sum ledger transaction amounts
    ApiResponse<Object> response = apiInstance.SumTransactionsWithHttpInfo(startDate, endDate, transactionType, segmentType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsApi.SumTransactionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDate** | **DateTime** |  |  |
| **endDate** | **DateTime** |  |  |
| **transactionType** | **string?** |  | [optional]  |
| **segmentType** | **string?** |  | [optional]  |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

