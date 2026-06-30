# WalletInc.Api.StaticVouchersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateStaticVoucher**](StaticVouchersApi.md#createstaticvoucher) | **POST** /v2/payment/staticVoucher | Create Static Voucher |
| [**DeleteStaticVoucher**](StaticVouchersApi.md#deletestaticvoucher) | **DELETE** /v2/payment/staticVoucher/{id} | Delete Static Voucher |
| [**FetchReachStatsOfAllStaticVouchers**](StaticVouchersApi.md#fetchreachstatsofallstaticvouchers) | **GET** /v2/payment/staticVoucher/reach/all | Get reach statistics of all Static Vouchers |
| [**FetchReachStatsOfIndividualStaticVoucher**](StaticVouchersApi.md#fetchreachstatsofindividualstaticvoucher) | **GET** /v2/payment/staticVoucher/reach/{staticVoucherID} | Get reach statistics of a single Static Voucher |
| [**FetchStaticVoucher**](StaticVouchersApi.md#fetchstaticvoucher) | **GET** /v2/payment/staticVoucher/{id} | Get Static Voucher |
| [**UpdateStaticVoucher**](StaticVouchersApi.md#updatestaticvoucher) | **PUT** /v2/payment/staticVoucher/{id} | Update Static Voucher |

<a id="createstaticvoucher"></a>
# **CreateStaticVoucher**
> WTStaticVoucher CreateStaticVoucher (WTStaticVoucherCreateParams wTStaticVoucherCreateParams)

Create Static Voucher

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
    public class CreateStaticVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVouchersApi(httpClient, config, httpClientHandler);
            var wTStaticVoucherCreateParams = new WTStaticVoucherCreateParams(); // WTStaticVoucherCreateParams | 

            try
            {
                // Create Static Voucher
                WTStaticVoucher result = apiInstance.CreateStaticVoucher(wTStaticVoucherCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVouchersApi.CreateStaticVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateStaticVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Static Voucher
    ApiResponse<WTStaticVoucher> response = apiInstance.CreateStaticVoucherWithHttpInfo(wTStaticVoucherCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVouchersApi.CreateStaticVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTStaticVoucherCreateParams** | [**WTStaticVoucherCreateParams**](WTStaticVoucherCreateParams.md) |  |  |

### Return type

[**WTStaticVoucher**](WTStaticVoucher.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Authentication Failed |  -  |
| **409** | Duplicate Row Found |  -  |
| **422** | Validation Failed |  -  |
| **424** | Merchant Not Initialized |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletestaticvoucher"></a>
# **DeleteStaticVoucher**
> bool DeleteStaticVoucher (string id)

Delete Static Voucher

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
    public class DeleteStaticVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVouchersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Delete Static Voucher
                bool result = apiInstance.DeleteStaticVoucher(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVouchersApi.DeleteStaticVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteStaticVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Static Voucher
    ApiResponse<bool> response = apiInstance.DeleteStaticVoucherWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVouchersApi.DeleteStaticVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

**bool**

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
| **409** | Duplicate Row Found |  -  |
| **422** | Validation Failed |  -  |
| **424** | Foreign Key does not exist |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchreachstatsofallstaticvouchers"></a>
# **FetchReachStatsOfAllStaticVouchers**
> ReachPerformanceStats FetchReachStatsOfAllStaticVouchers (DateTime? broadcastScheduledStartAt = null, DateTime? broadcastScheduledEndAt = null)

Get reach statistics of all Static Vouchers

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
    public class FetchReachStatsOfAllStaticVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVouchersApi(httpClient, config, httpClientHandler);
            var broadcastScheduledStartAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var broadcastScheduledEndAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get reach statistics of all Static Vouchers
                ReachPerformanceStats result = apiInstance.FetchReachStatsOfAllStaticVouchers(broadcastScheduledStartAt, broadcastScheduledEndAt);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVouchersApi.FetchReachStatsOfAllStaticVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchReachStatsOfAllStaticVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get reach statistics of all Static Vouchers
    ApiResponse<ReachPerformanceStats> response = apiInstance.FetchReachStatsOfAllStaticVouchersWithHttpInfo(broadcastScheduledStartAt, broadcastScheduledEndAt);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVouchersApi.FetchReachStatsOfAllStaticVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **broadcastScheduledStartAt** | **DateTime?** |  | [optional]  |
| **broadcastScheduledEndAt** | **DateTime?** |  | [optional]  |

### Return type

[**ReachPerformanceStats**](ReachPerformanceStats.md)

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

<a id="fetchreachstatsofindividualstaticvoucher"></a>
# **FetchReachStatsOfIndividualStaticVoucher**
> ReachPerformanceStats FetchReachStatsOfIndividualStaticVoucher (string staticVoucherID, DateTime? broadcastScheduledStartAt = null, DateTime? broadcastScheduledEndAt = null)

Get reach statistics of a single Static Voucher

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
    public class FetchReachStatsOfIndividualStaticVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVouchersApi(httpClient, config, httpClientHandler);
            var staticVoucherID = "staticVoucherID_example";  // string | 
            var broadcastScheduledStartAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var broadcastScheduledEndAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get reach statistics of a single Static Voucher
                ReachPerformanceStats result = apiInstance.FetchReachStatsOfIndividualStaticVoucher(staticVoucherID, broadcastScheduledStartAt, broadcastScheduledEndAt);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVouchersApi.FetchReachStatsOfIndividualStaticVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchReachStatsOfIndividualStaticVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get reach statistics of a single Static Voucher
    ApiResponse<ReachPerformanceStats> response = apiInstance.FetchReachStatsOfIndividualStaticVoucherWithHttpInfo(staticVoucherID, broadcastScheduledStartAt, broadcastScheduledEndAt);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVouchersApi.FetchReachStatsOfIndividualStaticVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **staticVoucherID** | **string** |  |  |
| **broadcastScheduledStartAt** | **DateTime?** |  | [optional]  |
| **broadcastScheduledEndAt** | **DateTime?** |  | [optional]  |

### Return type

[**ReachPerformanceStats**](ReachPerformanceStats.md)

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

<a id="fetchstaticvoucher"></a>
# **FetchStaticVoucher**
> WTStaticVoucher FetchStaticVoucher (string id)

Get Static Voucher

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
    public class FetchStaticVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVouchersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Static Voucher
                WTStaticVoucher result = apiInstance.FetchStaticVoucher(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVouchersApi.FetchStaticVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchStaticVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Static Voucher
    ApiResponse<WTStaticVoucher> response = apiInstance.FetchStaticVoucherWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVouchersApi.FetchStaticVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTStaticVoucher**](WTStaticVoucher.md)

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
| **424** | Foreign Key does not exist |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatestaticvoucher"></a>
# **UpdateStaticVoucher**
> WTStaticVoucher UpdateStaticVoucher (string id, WTStaticVoucherUpdateParams wTStaticVoucherUpdateParams)

Update Static Voucher

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
    public class UpdateStaticVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVouchersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTStaticVoucherUpdateParams = new WTStaticVoucherUpdateParams(); // WTStaticVoucherUpdateParams | 

            try
            {
                // Update Static Voucher
                WTStaticVoucher result = apiInstance.UpdateStaticVoucher(id, wTStaticVoucherUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVouchersApi.UpdateStaticVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateStaticVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Static Voucher
    ApiResponse<WTStaticVoucher> response = apiInstance.UpdateStaticVoucherWithHttpInfo(id, wTStaticVoucherUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVouchersApi.UpdateStaticVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTStaticVoucherUpdateParams** | [**WTStaticVoucherUpdateParams**](WTStaticVoucherUpdateParams.md) |  |  |

### Return type

[**WTStaticVoucher**](WTStaticVoucher.md)

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
| **409** | Duplicate Row Found |  -  |
| **422** | Validation Failed |  -  |
| **424** | Foreign Key does not exist |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

