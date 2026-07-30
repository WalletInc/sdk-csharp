# WalletInc.Api.GoogleWalletSubscribersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchGoogleWalletSubscriberActivity**](GoogleWalletSubscribersApi.md#fetchgooglewalletsubscriberactivity) | **GET** /google/wallet/pass/subscriber/activity/{subscriptionID} | Get subscriber activity Scoped to the caller&#39;s merchant: the subscription must belong to them (tightening the Apple sibling, which does not re-check ownership on this route). |
| [**FetchGoogleWalletSubscribers**](GoogleWalletSubscribersApi.md#fetchgooglewalletsubscribers) | **GET** /google/wallet/pass/subscribers/all | Get all subscribers |

<a id="fetchgooglewalletsubscriberactivity"></a>
# **FetchGoogleWalletSubscriberActivity**
> List&lt;Object&gt; FetchGoogleWalletSubscriberActivity (string subscriptionID)

Get subscriber activity Scoped to the caller's merchant: the subscription must belong to them (tightening the Apple sibling, which does not re-check ownership on this route).

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
    public class FetchGoogleWalletSubscriberActivityExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GoogleWalletSubscribersApi(httpClient, config, httpClientHandler);
            var subscriptionID = "subscriptionID_example";  // string | 

            try
            {
                // Get subscriber activity Scoped to the caller's merchant: the subscription must belong to them (tightening the Apple sibling, which does not re-check ownership on this route).
                List<Object> result = apiInstance.FetchGoogleWalletSubscriberActivity(subscriptionID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleWalletSubscribersApi.FetchGoogleWalletSubscriberActivity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchGoogleWalletSubscriberActivityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get subscriber activity Scoped to the caller's merchant: the subscription must belong to them (tightening the Apple sibling, which does not re-check ownership on this route).
    ApiResponse<List<Object>> response = apiInstance.FetchGoogleWalletSubscriberActivityWithHttpInfo(subscriptionID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleWalletSubscribersApi.FetchGoogleWalletSubscriberActivityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **subscriptionID** | **string** |  |  |

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

<a id="fetchgooglewalletsubscribers"></a>
# **FetchGoogleWalletSubscribers**
> List&lt;Object&gt; FetchGoogleWalletSubscribers (DateTime? startDateTime = null, DateTime? endDateTime = null)

Get all subscribers

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
    public class FetchGoogleWalletSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GoogleWalletSubscribersApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get all subscribers
                List<Object> result = apiInstance.FetchGoogleWalletSubscribers(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleWalletSubscribersApi.FetchGoogleWalletSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchGoogleWalletSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all subscribers
    ApiResponse<List<Object>> response = apiInstance.FetchGoogleWalletSubscribersWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleWalletSubscribersApi.FetchGoogleWalletSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime?** |  | [optional]  |
| **endDateTime** | **DateTime?** |  | [optional]  |

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

