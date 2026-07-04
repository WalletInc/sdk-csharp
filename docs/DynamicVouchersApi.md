# WalletInc.Api.DynamicVouchersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveDynamicVoucherCampaign**](DynamicVouchersApi.md#archivedynamicvouchercampaign) | **DELETE** /v2/payment/dynamicVoucher/{campaignID} | Archive Dynamic Voucher Campaign |
| [**CreateDynamicVoucher**](DynamicVouchersApi.md#createdynamicvoucher) | **POST** /v2/payment/dynamicVoucher | Create Dynamic Voucher Campaign |
| [**FetchAllDynamicVouchers**](DynamicVouchersApi.md#fetchalldynamicvouchers) | **GET** /v2/payment/dynamicVoucher/all | Get all Dynamic Voucher Campaigns |
| [**FetchDynamicVoucherById**](DynamicVouchersApi.md#fetchdynamicvoucherbyid) | **GET** /v2/payment/dynamicVoucher/{id} | Get Dynamic Voucher Campaign |
| [**FetchDynamicVoucherRedemptions**](DynamicVouchersApi.md#fetchdynamicvoucherredemptions) | **GET** /v2/payment/dynamicVoucher/redemptions/{id} | Get Dynamic Voucher Campaign Redemptions |
| [**FetchDynamicVouchers**](DynamicVouchersApi.md#fetchdynamicvouchers) | **GET** /v2/employee/dynamicVouchers/all | Get all dynamic vouchers |
| [**FetchReachStatsOfAllDynamicVouchers**](DynamicVouchersApi.md#fetchreachstatsofalldynamicvouchers) | **GET** /v2/payment/dynamicVoucher/reach/all | Get the reach statistics of all the dynamic vouchers |
| [**FetchReachStatsOfIndividualDynamicVoucher**](DynamicVouchersApi.md#fetchreachstatsofindividualdynamicvoucher) | **GET** /v2/payment/dynamicVoucher/reach/{dynamicVoucherID} | Get the reach statistics of an individual dynamic voucher |
| [**RestoreDynamicVoucherCampaign**](DynamicVouchersApi.md#restoredynamicvouchercampaign) | **PATCH** /v2/payment/dynamicVoucher/{campaignID} | Restore Dynamic Voucher Campaign |
| [**SaveDynamicVoucher**](DynamicVouchersApi.md#savedynamicvoucher) | **PUT** /v2/payment/dynamicVoucher/{id} | Update Dynamic Voucher Campaign |

<a id="archivedynamicvouchercampaign"></a>
# **ArchiveDynamicVoucherCampaign**
> DynamicVoucher ArchiveDynamicVoucherCampaign (string campaignID)

Archive Dynamic Voucher Campaign

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
    public class ArchiveDynamicVoucherCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Archive Dynamic Voucher Campaign
                DynamicVoucher result = apiInstance.ArchiveDynamicVoucherCampaign(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.ArchiveDynamicVoucherCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveDynamicVoucherCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Dynamic Voucher Campaign
    ApiResponse<DynamicVoucher> response = apiInstance.ArchiveDynamicVoucherCampaignWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.ArchiveDynamicVoucherCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**DynamicVoucher**](DynamicVoucher.md)

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

<a id="createdynamicvoucher"></a>
# **CreateDynamicVoucher**
> WTDynamicVoucher CreateDynamicVoucher (WTDynamicVoucherCreateParams wTDynamicVoucherCreateParams)

Create Dynamic Voucher Campaign

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
    public class CreateDynamicVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var wTDynamicVoucherCreateParams = new WTDynamicVoucherCreateParams(); // WTDynamicVoucherCreateParams | 

            try
            {
                // Create Dynamic Voucher Campaign
                WTDynamicVoucher result = apiInstance.CreateDynamicVoucher(wTDynamicVoucherCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.CreateDynamicVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDynamicVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Dynamic Voucher Campaign
    ApiResponse<WTDynamicVoucher> response = apiInstance.CreateDynamicVoucherWithHttpInfo(wTDynamicVoucherCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.CreateDynamicVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTDynamicVoucherCreateParams** | [**WTDynamicVoucherCreateParams**](WTDynamicVoucherCreateParams.md) |  |  |

### Return type

[**WTDynamicVoucher**](WTDynamicVoucher.md)

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

<a id="fetchalldynamicvouchers"></a>
# **FetchAllDynamicVouchers**
> List&lt;WTDynamicVoucher&gt; FetchAllDynamicVouchers (bool? isArchiveIncluded = null)

Get all Dynamic Voucher Campaigns

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
    public class FetchAllDynamicVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all Dynamic Voucher Campaigns
                List<WTDynamicVoucher> result = apiInstance.FetchAllDynamicVouchers(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.FetchAllDynamicVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllDynamicVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Dynamic Voucher Campaigns
    ApiResponse<List<WTDynamicVoucher>> response = apiInstance.FetchAllDynamicVouchersWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.FetchAllDynamicVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;WTDynamicVoucher&gt;**](WTDynamicVoucher.md)

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

<a id="fetchdynamicvoucherbyid"></a>
# **FetchDynamicVoucherById**
> WTDynamicVoucher FetchDynamicVoucherById (string id)

Get Dynamic Voucher Campaign

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
    public class FetchDynamicVoucherByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Dynamic Voucher Campaign
                WTDynamicVoucher result = apiInstance.FetchDynamicVoucherById(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.FetchDynamicVoucherById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDynamicVoucherByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Dynamic Voucher Campaign
    ApiResponse<WTDynamicVoucher> response = apiInstance.FetchDynamicVoucherByIdWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.FetchDynamicVoucherByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTDynamicVoucher**](WTDynamicVoucher.md)

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

<a id="fetchdynamicvoucherredemptions"></a>
# **FetchDynamicVoucherRedemptions**
> List&lt;WTDynamicVoucherRedemption&gt; FetchDynamicVoucherRedemptions (string id)

Get Dynamic Voucher Campaign Redemptions

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
    public class FetchDynamicVoucherRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Dynamic Voucher Campaign Redemptions
                List<WTDynamicVoucherRedemption> result = apiInstance.FetchDynamicVoucherRedemptions(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.FetchDynamicVoucherRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDynamicVoucherRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Dynamic Voucher Campaign Redemptions
    ApiResponse<List<WTDynamicVoucherRedemption>> response = apiInstance.FetchDynamicVoucherRedemptionsWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.FetchDynamicVoucherRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**List&lt;WTDynamicVoucherRedemption&gt;**](WTDynamicVoucherRedemption.md)

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

<a id="fetchdynamicvouchers"></a>
# **FetchDynamicVouchers**
> List&lt;DynamicVoucher&gt; FetchDynamicVouchers (bool? isArchiveIncluded = null)

Get all dynamic vouchers

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
    public class FetchDynamicVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all dynamic vouchers
                List<DynamicVoucher> result = apiInstance.FetchDynamicVouchers(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.FetchDynamicVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDynamicVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all dynamic vouchers
    ApiResponse<List<DynamicVoucher>> response = apiInstance.FetchDynamicVouchersWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.FetchDynamicVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;DynamicVoucher&gt;**](DynamicVoucher.md)

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

<a id="fetchreachstatsofalldynamicvouchers"></a>
# **FetchReachStatsOfAllDynamicVouchers**
> ReachPerformanceStats FetchReachStatsOfAllDynamicVouchers (DateTime? broadcastScheduledStartAt = null, DateTime? broadcastScheduledEndAt = null)

Get the reach statistics of all the dynamic vouchers

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
    public class FetchReachStatsOfAllDynamicVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var broadcastScheduledStartAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var broadcastScheduledEndAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get the reach statistics of all the dynamic vouchers
                ReachPerformanceStats result = apiInstance.FetchReachStatsOfAllDynamicVouchers(broadcastScheduledStartAt, broadcastScheduledEndAt);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.FetchReachStatsOfAllDynamicVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchReachStatsOfAllDynamicVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get the reach statistics of all the dynamic vouchers
    ApiResponse<ReachPerformanceStats> response = apiInstance.FetchReachStatsOfAllDynamicVouchersWithHttpInfo(broadcastScheduledStartAt, broadcastScheduledEndAt);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.FetchReachStatsOfAllDynamicVouchersWithHttpInfo: " + e.Message);
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

<a id="fetchreachstatsofindividualdynamicvoucher"></a>
# **FetchReachStatsOfIndividualDynamicVoucher**
> ReachPerformanceStats FetchReachStatsOfIndividualDynamicVoucher (string dynamicVoucherID, DateTime? broadcastScheduledStartAt = null, DateTime? broadcastScheduledEndAt = null)

Get the reach statistics of an individual dynamic voucher

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
    public class FetchReachStatsOfIndividualDynamicVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var dynamicVoucherID = "dynamicVoucherID_example";  // string | 
            var broadcastScheduledStartAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var broadcastScheduledEndAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get the reach statistics of an individual dynamic voucher
                ReachPerformanceStats result = apiInstance.FetchReachStatsOfIndividualDynamicVoucher(dynamicVoucherID, broadcastScheduledStartAt, broadcastScheduledEndAt);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.FetchReachStatsOfIndividualDynamicVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchReachStatsOfIndividualDynamicVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get the reach statistics of an individual dynamic voucher
    ApiResponse<ReachPerformanceStats> response = apiInstance.FetchReachStatsOfIndividualDynamicVoucherWithHttpInfo(dynamicVoucherID, broadcastScheduledStartAt, broadcastScheduledEndAt);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.FetchReachStatsOfIndividualDynamicVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dynamicVoucherID** | **string** |  |  |
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

<a id="restoredynamicvouchercampaign"></a>
# **RestoreDynamicVoucherCampaign**
> DynamicVoucher RestoreDynamicVoucherCampaign (string campaignID)

Restore Dynamic Voucher Campaign

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
    public class RestoreDynamicVoucherCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Restore Dynamic Voucher Campaign
                DynamicVoucher result = apiInstance.RestoreDynamicVoucherCampaign(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.RestoreDynamicVoucherCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreDynamicVoucherCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Dynamic Voucher Campaign
    ApiResponse<DynamicVoucher> response = apiInstance.RestoreDynamicVoucherCampaignWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.RestoreDynamicVoucherCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**DynamicVoucher**](DynamicVoucher.md)

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

<a id="savedynamicvoucher"></a>
# **SaveDynamicVoucher**
> WTDynamicVoucher SaveDynamicVoucher (string id, WTDynamicVoucherUpdateParams wTDynamicVoucherUpdateParams)

Update Dynamic Voucher Campaign

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
    public class SaveDynamicVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DynamicVouchersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTDynamicVoucherUpdateParams = new WTDynamicVoucherUpdateParams(); // WTDynamicVoucherUpdateParams | 

            try
            {
                // Update Dynamic Voucher Campaign
                WTDynamicVoucher result = apiInstance.SaveDynamicVoucher(id, wTDynamicVoucherUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DynamicVouchersApi.SaveDynamicVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveDynamicVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Dynamic Voucher Campaign
    ApiResponse<WTDynamicVoucher> response = apiInstance.SaveDynamicVoucherWithHttpInfo(id, wTDynamicVoucherUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DynamicVouchersApi.SaveDynamicVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTDynamicVoucherUpdateParams** | [**WTDynamicVoucherUpdateParams**](WTDynamicVoucherUpdateParams.md) |  |  |

### Return type

[**WTDynamicVoucher**](WTDynamicVoucher.md)

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

