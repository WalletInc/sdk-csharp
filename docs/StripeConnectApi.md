# WalletInc.Api.StripeConnectApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateConnectOnboardingLink**](StripeConnectApi.md#createconnectonboardinglink) | **POST** /v2/connect/account/onboarding-link | Create a Stripe Connect onboarding link Creates the merchant&#39;s STANDARD connected account on first call (pass-through model; the merchant owns their Stripe relationship) and returns a hosted onboarding link (single-use, expiring). returnUrl/refreshUrl are validated against the origin allowlist. Not a fund-moving write; 403 when the merchant&#39;s plan does not include Connect ecommerce. |
| [**FetchConnectAccountStatus**](StripeConnectApi.md#fetchconnectaccountstatus) | **GET** /v2/connect/account | Get Stripe Connect account status Observability for Flow B ecommerce: the connected-account id and capability flags for the authenticated merchant, plus the derived onboarding status and the server-side ecommerce eligibility flag. Returns the defined not-started shape (accountId null) rather than 404 when onboarding has not begun. |
| [**FetchConnectPaymentsSummary**](StripeConnectApi.md#fetchconnectpaymentssummary) | **GET** /v2/connect/payments-summary | Get a read-only Connect payments summary Balances, recent payouts, and recent charges (up to 10 each) for the merchant&#39;s connected account, in Stripe minor units with currency codes. Read-only observability; Wallet is not in the Flow B money path. |

<a id="createconnectonboardinglink"></a>
# **CreateConnectOnboardingLink**
> WTConnectOnboardingLinkResponse CreateConnectOnboardingLink (WTConnectOnboardingLinkRequest wTConnectOnboardingLinkRequest)

Create a Stripe Connect onboarding link Creates the merchant's STANDARD connected account on first call (pass-through model; the merchant owns their Stripe relationship) and returns a hosted onboarding link (single-use, expiring). returnUrl/refreshUrl are validated against the origin allowlist. Not a fund-moving write; 403 when the merchant's plan does not include Connect ecommerce.

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
    public class CreateConnectOnboardingLinkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StripeConnectApi(httpClient, config, httpClientHandler);
            var wTConnectOnboardingLinkRequest = new WTConnectOnboardingLinkRequest(); // WTConnectOnboardingLinkRequest | 

            try
            {
                // Create a Stripe Connect onboarding link Creates the merchant's STANDARD connected account on first call (pass-through model; the merchant owns their Stripe relationship) and returns a hosted onboarding link (single-use, expiring). returnUrl/refreshUrl are validated against the origin allowlist. Not a fund-moving write; 403 when the merchant's plan does not include Connect ecommerce.
                WTConnectOnboardingLinkResponse result = apiInstance.CreateConnectOnboardingLink(wTConnectOnboardingLinkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StripeConnectApi.CreateConnectOnboardingLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateConnectOnboardingLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a Stripe Connect onboarding link Creates the merchant's STANDARD connected account on first call (pass-through model; the merchant owns their Stripe relationship) and returns a hosted onboarding link (single-use, expiring). returnUrl/refreshUrl are validated against the origin allowlist. Not a fund-moving write; 403 when the merchant's plan does not include Connect ecommerce.
    ApiResponse<WTConnectOnboardingLinkResponse> response = apiInstance.CreateConnectOnboardingLinkWithHttpInfo(wTConnectOnboardingLinkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StripeConnectApi.CreateConnectOnboardingLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTConnectOnboardingLinkRequest** | [**WTConnectOnboardingLinkRequest**](WTConnectOnboardingLinkRequest.md) |  |  |

### Return type

[**WTConnectOnboardingLinkResponse**](WTConnectOnboardingLinkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchconnectaccountstatus"></a>
# **FetchConnectAccountStatus**
> WTConnectAccountStatus FetchConnectAccountStatus ()

Get Stripe Connect account status Observability for Flow B ecommerce: the connected-account id and capability flags for the authenticated merchant, plus the derived onboarding status and the server-side ecommerce eligibility flag. Returns the defined not-started shape (accountId null) rather than 404 when onboarding has not begun.

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
    public class FetchConnectAccountStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StripeConnectApi(httpClient, config, httpClientHandler);

            try
            {
                // Get Stripe Connect account status Observability for Flow B ecommerce: the connected-account id and capability flags for the authenticated merchant, plus the derived onboarding status and the server-side ecommerce eligibility flag. Returns the defined not-started shape (accountId null) rather than 404 when onboarding has not begun.
                WTConnectAccountStatus result = apiInstance.FetchConnectAccountStatus();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StripeConnectApi.FetchConnectAccountStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchConnectAccountStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Stripe Connect account status Observability for Flow B ecommerce: the connected-account id and capability flags for the authenticated merchant, plus the derived onboarding status and the server-side ecommerce eligibility flag. Returns the defined not-started shape (accountId null) rather than 404 when onboarding has not begun.
    ApiResponse<WTConnectAccountStatus> response = apiInstance.FetchConnectAccountStatusWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StripeConnectApi.FetchConnectAccountStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**WTConnectAccountStatus**](WTConnectAccountStatus.md)

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

<a id="fetchconnectpaymentssummary"></a>
# **FetchConnectPaymentsSummary**
> WTConnectPaymentsSummary FetchConnectPaymentsSummary ()

Get a read-only Connect payments summary Balances, recent payouts, and recent charges (up to 10 each) for the merchant's connected account, in Stripe minor units with currency codes. Read-only observability; Wallet is not in the Flow B money path.

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
    public class FetchConnectPaymentsSummaryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StripeConnectApi(httpClient, config, httpClientHandler);

            try
            {
                // Get a read-only Connect payments summary Balances, recent payouts, and recent charges (up to 10 each) for the merchant's connected account, in Stripe minor units with currency codes. Read-only observability; Wallet is not in the Flow B money path.
                WTConnectPaymentsSummary result = apiInstance.FetchConnectPaymentsSummary();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StripeConnectApi.FetchConnectPaymentsSummary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchConnectPaymentsSummaryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a read-only Connect payments summary Balances, recent payouts, and recent charges (up to 10 each) for the merchant's connected account, in Stripe minor units with currency codes. Read-only observability; Wallet is not in the Flow B money path.
    ApiResponse<WTConnectPaymentsSummary> response = apiInstance.FetchConnectPaymentsSummaryWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StripeConnectApi.FetchConnectPaymentsSummaryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**WTConnectPaymentsSummary**](WTConnectPaymentsSummary.md)

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

