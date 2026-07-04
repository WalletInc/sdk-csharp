# WalletInc.Api.DashboardSummariesApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CountTotalWalletSessions**](DashboardSummariesApi.md#counttotalwalletsessions) | **GET** /v2/dashboard/count/visitors | Count new sessions |
| [**FetchDashboardActiveStaticVouchersCount**](DashboardSummariesApi.md#fetchdashboardactivestaticvoucherscount) | **GET** /v2/dashboard/count/staticVouchers/active | Count active static vouchers |
| [**FetchDashboardAppleWalletSubscribersCount**](DashboardSummariesApi.md#fetchdashboardapplewalletsubscriberscount) | **GET** /v2/dashboard/count/appleWallet/subscribers | Count Apple Wallet Subscribers |
| [**FetchDashboardEmployeesCount**](DashboardSummariesApi.md#fetchdashboardemployeescount) | **GET** /v2/dashboard/count/employees | Count employees |
| [**FetchDashboardMembersCount**](DashboardSummariesApi.md#fetchdashboardmemberscount) | **GET** /v2/dashboard/count/members | Count members |
| [**FetchDashboardMembershipTiersCount**](DashboardSummariesApi.md#fetchdashboardmembershiptierscount) | **GET** /v2/dashboard/count/membershipTiers | Count tiers |
| [**FetchDashboardNewsArticlesCount**](DashboardSummariesApi.md#fetchdashboardnewsarticlescount) | **GET** /v2/dashboard/count/newsArticles | Count News Articles |
| [**FetchDashboardOptInListsCount**](DashboardSummariesApi.md#fetchdashboardoptinlistscount) | **GET** /v2/dashboard/count/optInLists | Count opt in lists |
| [**FetchDashboardOptInSourcesCount**](DashboardSummariesApi.md#fetchdashboardoptinsourcescount) | **GET** /v2/dashboard/count/optInSources | Count opt in sources |
| [**FetchDashboardOutboundSMSCount**](DashboardSummariesApi.md#fetchdashboardoutboundsmscount) | **GET** /v2/dashboard/count/sms/outbound | Count Outbound SMS |
| [**FetchDashboardPOSMachinesCount**](DashboardSummariesApi.md#fetchdashboardposmachinescount) | **GET** /v2/dashboard/count/pos/machines | Count POS Machines |
| [**FetchDashboardPOSTransactionsCount**](DashboardSummariesApi.md#fetchdashboardpostransactionscount) | **GET** /v2/dashboard/count/pos/transactions | Count POS Transactions |
| [**FetchDashboardPerformancesCount**](DashboardSummariesApi.md#fetchdashboardperformancescount) | **GET** /v2/dashboard/count/performances | Count Performances |
| [**FetchDashboardPhoneNumbersCount**](DashboardSummariesApi.md#fetchdashboardphonenumberscount) | **GET** /v2/dashboard/count/phoneNumbers | Count phone numbers |
| [**FetchDashboardRedemptionsCount**](DashboardSummariesApi.md#fetchdashboardredemptionscount) | **GET** /v2/dashboard/count/pos/redemptions | Count POS redemptions |
| [**FetchDashboardRefundsCount**](DashboardSummariesApi.md#fetchdashboardrefundscount) | **GET** /v2/dashboard/count/pos/refunds | Count POS refunds |
| [**FetchDashboardWalletPageViewsCount**](DashboardSummariesApi.md#fetchdashboardwalletpageviewscount) | **GET** /v2/dashboard/count/wallet/pageViews | Count Wallet page views |
| [**FetchSubscriberCount**](DashboardSummariesApi.md#fetchsubscribercount) | **GET** /v2/dashboard/count/subscribers | Count subscribers |

<a id="counttotalwalletsessions"></a>
# **CountTotalWalletSessions**
> WTCountResult CountTotalWalletSessions (DateTime? startDate = null, DateTime? endDate = null)

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
    public class CountTotalWalletSessionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count new sessions
                WTCountResult result = apiInstance.CountTotalWalletSessions(startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.CountTotalWalletSessions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountTotalWalletSessionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count new sessions
    ApiResponse<WTCountResult> response = apiInstance.CountTotalWalletSessionsWithHttpInfo(startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.CountTotalWalletSessionsWithHttpInfo: " + e.Message);
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

<a id="fetchdashboardactivestaticvoucherscount"></a>
# **FetchDashboardActiveStaticVouchersCount**
> WTCountResult FetchDashboardActiveStaticVouchersCount (DateTime startDateTime, DateTime endDateTime)

Count active static vouchers

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
    public class FetchDashboardActiveStaticVouchersCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count active static vouchers
                WTCountResult result = apiInstance.FetchDashboardActiveStaticVouchersCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardActiveStaticVouchersCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardActiveStaticVouchersCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count active static vouchers
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardActiveStaticVouchersCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardActiveStaticVouchersCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardapplewalletsubscriberscount"></a>
# **FetchDashboardAppleWalletSubscribersCount**
> WTCountResult FetchDashboardAppleWalletSubscribersCount (DateTime startDateTime, DateTime endDateTime)

Count Apple Wallet Subscribers

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
    public class FetchDashboardAppleWalletSubscribersCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count Apple Wallet Subscribers
                WTCountResult result = apiInstance.FetchDashboardAppleWalletSubscribersCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardAppleWalletSubscribersCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardAppleWalletSubscribersCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count Apple Wallet Subscribers
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardAppleWalletSubscribersCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardAppleWalletSubscribersCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardemployeescount"></a>
# **FetchDashboardEmployeesCount**
> WTCountResult FetchDashboardEmployeesCount (DateTime startDateTime, DateTime endDateTime)

Count employees

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
    public class FetchDashboardEmployeesCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count employees
                WTCountResult result = apiInstance.FetchDashboardEmployeesCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardEmployeesCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardEmployeesCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count employees
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardEmployeesCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardEmployeesCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardmemberscount"></a>
# **FetchDashboardMembersCount**
> WTCountResult FetchDashboardMembersCount (DateTime startDateTime, DateTime endDateTime)

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
    public class FetchDashboardMembersCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count members
                WTCountResult result = apiInstance.FetchDashboardMembersCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardMembersCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardMembersCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count members
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardMembersCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardMembersCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardmembershiptierscount"></a>
# **FetchDashboardMembershipTiersCount**
> WTCountResult FetchDashboardMembershipTiersCount (DateTime startDateTime, DateTime endDateTime)

Count tiers

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
    public class FetchDashboardMembershipTiersCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count tiers
                WTCountResult result = apiInstance.FetchDashboardMembershipTiersCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardMembershipTiersCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardMembershipTiersCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count tiers
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardMembershipTiersCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardMembershipTiersCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardnewsarticlescount"></a>
# **FetchDashboardNewsArticlesCount**
> WTCountResult FetchDashboardNewsArticlesCount (DateTime startDateTime, DateTime endDateTime)

Count News Articles

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
    public class FetchDashboardNewsArticlesCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count News Articles
                WTCountResult result = apiInstance.FetchDashboardNewsArticlesCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardNewsArticlesCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardNewsArticlesCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count News Articles
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardNewsArticlesCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardNewsArticlesCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardoptinlistscount"></a>
# **FetchDashboardOptInListsCount**
> WTCountResult FetchDashboardOptInListsCount (DateTime startDateTime, DateTime endDateTime)

Count opt in lists

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
    public class FetchDashboardOptInListsCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count opt in lists
                WTCountResult result = apiInstance.FetchDashboardOptInListsCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardOptInListsCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardOptInListsCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count opt in lists
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardOptInListsCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardOptInListsCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardoptinsourcescount"></a>
# **FetchDashboardOptInSourcesCount**
> WTCountResult FetchDashboardOptInSourcesCount (DateTime startDateTime, DateTime endDateTime)

Count opt in sources

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
    public class FetchDashboardOptInSourcesCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count opt in sources
                WTCountResult result = apiInstance.FetchDashboardOptInSourcesCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardOptInSourcesCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardOptInSourcesCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count opt in sources
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardOptInSourcesCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardOptInSourcesCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardoutboundsmscount"></a>
# **FetchDashboardOutboundSMSCount**
> WTCountResult FetchDashboardOutboundSMSCount (DateTime startDateTime, DateTime endDateTime)

Count Outbound SMS

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
    public class FetchDashboardOutboundSMSCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count Outbound SMS
                WTCountResult result = apiInstance.FetchDashboardOutboundSMSCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardOutboundSMSCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardOutboundSMSCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count Outbound SMS
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardOutboundSMSCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardOutboundSMSCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardposmachinescount"></a>
# **FetchDashboardPOSMachinesCount**
> WTCountResult FetchDashboardPOSMachinesCount (DateTime startDateTime, DateTime endDateTime)

Count POS Machines

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
    public class FetchDashboardPOSMachinesCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count POS Machines
                WTCountResult result = apiInstance.FetchDashboardPOSMachinesCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardPOSMachinesCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardPOSMachinesCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count POS Machines
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardPOSMachinesCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardPOSMachinesCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardpostransactionscount"></a>
# **FetchDashboardPOSTransactionsCount**
> WTCountResult FetchDashboardPOSTransactionsCount (DateTime startDateTime, DateTime endDateTime)

Count POS Transactions

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
    public class FetchDashboardPOSTransactionsCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count POS Transactions
                WTCountResult result = apiInstance.FetchDashboardPOSTransactionsCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardPOSTransactionsCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardPOSTransactionsCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count POS Transactions
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardPOSTransactionsCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardPOSTransactionsCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardperformancescount"></a>
# **FetchDashboardPerformancesCount**
> WTCountResult FetchDashboardPerformancesCount (DateTime startDateTime, DateTime endDateTime)

Count Performances

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
    public class FetchDashboardPerformancesCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count Performances
                WTCountResult result = apiInstance.FetchDashboardPerformancesCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardPerformancesCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardPerformancesCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count Performances
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardPerformancesCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardPerformancesCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardphonenumberscount"></a>
# **FetchDashboardPhoneNumbersCount**
> WTCountResult FetchDashboardPhoneNumbersCount (DateTime startDateTime, DateTime endDateTime)

Count phone numbers

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
    public class FetchDashboardPhoneNumbersCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count phone numbers
                WTCountResult result = apiInstance.FetchDashboardPhoneNumbersCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardPhoneNumbersCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardPhoneNumbersCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count phone numbers
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardPhoneNumbersCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardPhoneNumbersCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardredemptionscount"></a>
# **FetchDashboardRedemptionsCount**
> WTCountResult FetchDashboardRedemptionsCount (DateTime startDateTime, DateTime endDateTime)

Count POS redemptions

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
    public class FetchDashboardRedemptionsCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count POS redemptions
                WTCountResult result = apiInstance.FetchDashboardRedemptionsCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardRedemptionsCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardRedemptionsCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count POS redemptions
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardRedemptionsCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardRedemptionsCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardrefundscount"></a>
# **FetchDashboardRefundsCount**
> WTCountResult FetchDashboardRefundsCount (DateTime startDateTime, DateTime endDateTime)

Count POS refunds

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
    public class FetchDashboardRefundsCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count POS refunds
                WTCountResult result = apiInstance.FetchDashboardRefundsCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardRefundsCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardRefundsCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count POS refunds
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardRefundsCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardRefundsCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

<a id="fetchdashboardwalletpageviewscount"></a>
# **FetchDashboardWalletPageViewsCount**
> WTCountResult FetchDashboardWalletPageViewsCount (DateTime startDateTime, DateTime endDateTime, string? walletObjectPrefix = null)

Count Wallet page views

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
    public class FetchDashboardWalletPageViewsCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var walletObjectPrefix = "walletObjectPrefix_example";  // string? |  (optional) 

            try
            {
                // Count Wallet page views
                WTCountResult result = apiInstance.FetchDashboardWalletPageViewsCount(startDateTime, endDateTime, walletObjectPrefix);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardWalletPageViewsCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDashboardWalletPageViewsCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count Wallet page views
    ApiResponse<WTCountResult> response = apiInstance.FetchDashboardWalletPageViewsCountWithHttpInfo(startDateTime, endDateTime, walletObjectPrefix);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchDashboardWalletPageViewsCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |
| **walletObjectPrefix** | **string?** |  | [optional]  |

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

<a id="fetchsubscribercount"></a>
# **FetchSubscriberCount**
> WTCountResult FetchSubscriberCount (DateTime startDateTime, DateTime endDateTime)

Count subscribers

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
    public class FetchSubscriberCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DashboardSummariesApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Count subscribers
                WTCountResult result = apiInstance.FetchSubscriberCount(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DashboardSummariesApi.FetchSubscriberCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchSubscriberCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count subscribers
    ApiResponse<WTCountResult> response = apiInstance.FetchSubscriberCountWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DashboardSummariesApi.FetchSubscriberCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

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

