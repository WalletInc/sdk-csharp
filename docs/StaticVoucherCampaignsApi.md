# WalletInc.Api.StaticVoucherCampaignsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveStaticVoucherCampaign**](StaticVoucherCampaignsApi.md#archivestaticvouchercampaign) | **DELETE** /v2/payment/staticVoucherCampaign/{campaignID} | Archive Static Voucher Campaign |
| [**CountVouchersLoaded**](StaticVoucherCampaignsApi.md#countvouchersloaded) | **GET** /v2/payment/staticVoucherCampaign/count/vouchers/loaded/{campaignID} | Count vouchers in Static Vouchers Campaign |
| [**CountVouchersRedeemed**](StaticVoucherCampaignsApi.md#countvouchersredeemed) | **GET** /v2/payment/staticVoucherCampaign/count/vouchers/redeemed/{campaignID} | Count redeemed vouchers in Static Vouchers Campaign |
| [**CreateStaticVoucherCampaign**](StaticVoucherCampaignsApi.md#createstaticvouchercampaign) | **POST** /v2/payment/staticVoucherCampaign | Create Static Voucher Campaign |
| [**CreateStaticVoucherCampaignFromCSV**](StaticVoucherCampaignsApi.md#createstaticvouchercampaignfromcsv) | **POST** /v2/payment/staticVoucherCampaign/csv | Import Static Voucher Campaign |
| [**CreateStaticVoucherCampaignWithVoucher**](StaticVoucherCampaignsApi.md#createstaticvouchercampaignwithvoucher) | **POST** /v2/payment/staticVoucherCampaign/voucher | Create Static Voucher Campaign with single voucher |
| [**DuplicateStaticVoucherCampaignById**](StaticVoucherCampaignsApi.md#duplicatestaticvouchercampaignbyid) | **POST** /v2/payment/staticVoucherCampaign/duplicate/{campaignID} | Duplicate Static Vouchers Campaign |
| [**FetchPerformanceOverview**](StaticVoucherCampaignsApi.md#fetchperformanceoverview) | **GET** /v2/payment/staticVoucherCampaign/overview/performance/{campaignID} | Get Static Voucher Campaign performance overview |
| [**FetchReachStatsOfAllStaticVoucherCampaigns**](StaticVoucherCampaignsApi.md#fetchreachstatsofallstaticvouchercampaigns) | **GET** /v2/payment/staticVoucherCampaign/reach/all | Get the reach statistics of all Static Voucher Campaigns |
| [**FetchReachStatsOfIndividualStaticVoucherCampaign**](StaticVoucherCampaignsApi.md#fetchreachstatsofindividualstaticvouchercampaign) | **GET** /v2/payment/staticVoucherCampaign/reach/{staticVoucherCampaignID} | Get the reach statistics of a single Static Voucher Campaign |
| [**FetchStaticVoucherCampaignById**](StaticVoucherCampaignsApi.md#fetchstaticvouchercampaignbyid) | **GET** /v2/payment/staticVoucherCampaign/{id} | Get Static Vouchers Campaign |
| [**FetchStaticVoucherCampaigns**](StaticVoucherCampaignsApi.md#fetchstaticvouchercampaigns) | **GET** /v2/payment/staticVoucherCampaign/all | Get all Static Vouchers Campaigns |
| [**FetchStaticVouchers**](StaticVoucherCampaignsApi.md#fetchstaticvouchers) | **GET** /v2/payment/staticVoucherCampaign/staticVouchers/{campaignID} | Get vouchers in Static Vouchers Campaign |
| [**FetchStaticVouchersPage**](StaticVoucherCampaignsApi.md#fetchstaticvoucherspage) | **GET** /v2/payment/staticVoucherCampaign/staticVouchers/page/{campaignID} | Get a page of vouchers in a Static Voucher Campaign |
| [**FetchViews**](StaticVoucherCampaignsApi.md#fetchviews) | **GET** /v2/payment/staticVoucherCampaign/views/{campaignID} | Get Static Vouchers Campaign traffic |
| [**FetchVouchersRedeemed**](StaticVoucherCampaignsApi.md#fetchvouchersredeemed) | **GET** /v2/payment/staticVoucherCampaign/vouchers/redeemed/{campaignID} | Get redeemed vouchers in Static Vouchers Campaign |
| [**PreviewMessagesByPage**](StaticVoucherCampaignsApi.md#previewmessagesbypage) | **PUT** /v2/payment/staticVoucherCampaign/preview/page/{campaignID} | Preview generated broadcast messages by page |
| [**RestoreStaticVoucherCampaign**](StaticVoucherCampaignsApi.md#restorestaticvouchercampaign) | **PATCH** /v2/payment/staticVoucherCampaign/{campaignID} | Restore Static Voucher Campaign |
| [**UpdateStaticVoucherCampaign**](StaticVoucherCampaignsApi.md#updatestaticvouchercampaign) | **PUT** /v2/payment/staticVoucherCampaign/{campaignID} | Update Static Voucher Campaign |
| [**UpdateStaticVoucherCampaignWithVoucher**](StaticVoucherCampaignsApi.md#updatestaticvouchercampaignwithvoucher) | **PUT** /v2/payment/staticVoucherCampaign/voucher/{campaignID} | Update Static Voucher Campaign with single voucher |

<a id="archivestaticvouchercampaign"></a>
# **ArchiveStaticVoucherCampaign**
> StaticVoucherCampaign ArchiveStaticVoucherCampaign (string campaignID)

Archive Static Voucher Campaign

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
    public class ArchiveStaticVoucherCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Archive Static Voucher Campaign
                StaticVoucherCampaign result = apiInstance.ArchiveStaticVoucherCampaign(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.ArchiveStaticVoucherCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveStaticVoucherCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Static Voucher Campaign
    ApiResponse<StaticVoucherCampaign> response = apiInstance.ArchiveStaticVoucherCampaignWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.ArchiveStaticVoucherCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**StaticVoucherCampaign**](StaticVoucherCampaign.md)

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

<a id="countvouchersloaded"></a>
# **CountVouchersLoaded**
> FetchMembersCount200Response CountVouchersLoaded (string campaignID)

Count vouchers in Static Vouchers Campaign

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
    public class CountVouchersLoadedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Count vouchers in Static Vouchers Campaign
                FetchMembersCount200Response result = apiInstance.CountVouchersLoaded(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.CountVouchersLoaded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountVouchersLoadedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count vouchers in Static Vouchers Campaign
    ApiResponse<FetchMembersCount200Response> response = apiInstance.CountVouchersLoadedWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.CountVouchersLoadedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**FetchMembersCount200Response**](FetchMembersCount200Response.md)

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

<a id="countvouchersredeemed"></a>
# **CountVouchersRedeemed**
> FetchMembersCount200Response CountVouchersRedeemed (string campaignID)

Count redeemed vouchers in Static Vouchers Campaign

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
    public class CountVouchersRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Count redeemed vouchers in Static Vouchers Campaign
                FetchMembersCount200Response result = apiInstance.CountVouchersRedeemed(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.CountVouchersRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountVouchersRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redeemed vouchers in Static Vouchers Campaign
    ApiResponse<FetchMembersCount200Response> response = apiInstance.CountVouchersRedeemedWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.CountVouchersRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**FetchMembersCount200Response**](FetchMembersCount200Response.md)

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

<a id="createstaticvouchercampaign"></a>
# **CreateStaticVoucherCampaign**
> WTStaticVoucherCampaign CreateStaticVoucherCampaign (CreateStaticVoucherCampaign createStaticVoucherCampaign)

Create Static Voucher Campaign

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
    public class CreateStaticVoucherCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var createStaticVoucherCampaign = new CreateStaticVoucherCampaign(); // CreateStaticVoucherCampaign | 

            try
            {
                // Create Static Voucher Campaign
                WTStaticVoucherCampaign result = apiInstance.CreateStaticVoucherCampaign(createStaticVoucherCampaign);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.CreateStaticVoucherCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateStaticVoucherCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Static Voucher Campaign
    ApiResponse<WTStaticVoucherCampaign> response = apiInstance.CreateStaticVoucherCampaignWithHttpInfo(createStaticVoucherCampaign);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.CreateStaticVoucherCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createStaticVoucherCampaign** | [**CreateStaticVoucherCampaign**](CreateStaticVoucherCampaign.md) |  |  |

### Return type

[**WTStaticVoucherCampaign**](WTStaticVoucherCampaign.md)

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

<a id="createstaticvouchercampaignfromcsv"></a>
# **CreateStaticVoucherCampaignFromCSV**
> WTStaticVoucherCampaign CreateStaticVoucherCampaignFromCSV (CreateStaticVoucherCampaignWithVoucherWithCSV createStaticVoucherCampaignWithVoucherWithCSV)

Import Static Voucher Campaign

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
    public class CreateStaticVoucherCampaignFromCSVExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var createStaticVoucherCampaignWithVoucherWithCSV = new CreateStaticVoucherCampaignWithVoucherWithCSV(); // CreateStaticVoucherCampaignWithVoucherWithCSV | 

            try
            {
                // Import Static Voucher Campaign
                WTStaticVoucherCampaign result = apiInstance.CreateStaticVoucherCampaignFromCSV(createStaticVoucherCampaignWithVoucherWithCSV);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.CreateStaticVoucherCampaignFromCSV: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateStaticVoucherCampaignFromCSVWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Import Static Voucher Campaign
    ApiResponse<WTStaticVoucherCampaign> response = apiInstance.CreateStaticVoucherCampaignFromCSVWithHttpInfo(createStaticVoucherCampaignWithVoucherWithCSV);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.CreateStaticVoucherCampaignFromCSVWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createStaticVoucherCampaignWithVoucherWithCSV** | [**CreateStaticVoucherCampaignWithVoucherWithCSV**](CreateStaticVoucherCampaignWithVoucherWithCSV.md) |  |  |

### Return type

[**WTStaticVoucherCampaign**](WTStaticVoucherCampaign.md)

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

<a id="createstaticvouchercampaignwithvoucher"></a>
# **CreateStaticVoucherCampaignWithVoucher**
> WTStaticVoucherCampaign CreateStaticVoucherCampaignWithVoucher (PickCreateStaticVoucherCampaignWithVoucherExcludeKeyofcreateStaticVoucherCampaignWithVoucherIsActive body)

Create Static Voucher Campaign with single voucher

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
    public class CreateStaticVoucherCampaignWithVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var body = new PickCreateStaticVoucherCampaignWithVoucherExcludeKeyofcreateStaticVoucherCampaignWithVoucherIsActive();  // PickCreateStaticVoucherCampaignWithVoucherExcludeKeyofcreateStaticVoucherCampaignWithVoucherIsActive | 

            try
            {
                // Create Static Voucher Campaign with single voucher
                WTStaticVoucherCampaign result = apiInstance.CreateStaticVoucherCampaignWithVoucher(body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.CreateStaticVoucherCampaignWithVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateStaticVoucherCampaignWithVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Static Voucher Campaign with single voucher
    ApiResponse<WTStaticVoucherCampaign> response = apiInstance.CreateStaticVoucherCampaignWithVoucherWithHttpInfo(body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.CreateStaticVoucherCampaignWithVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **body** | **PickCreateStaticVoucherCampaignWithVoucherExcludeKeyofcreateStaticVoucherCampaignWithVoucherIsActive** |  |  |

### Return type

[**WTStaticVoucherCampaign**](WTStaticVoucherCampaign.md)

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

<a id="duplicatestaticvouchercampaignbyid"></a>
# **DuplicateStaticVoucherCampaignById**
> WTStaticVoucherCampaign DuplicateStaticVoucherCampaignById (string campaignID)

Duplicate Static Vouchers Campaign

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
    public class DuplicateStaticVoucherCampaignByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Duplicate Static Vouchers Campaign
                WTStaticVoucherCampaign result = apiInstance.DuplicateStaticVoucherCampaignById(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.DuplicateStaticVoucherCampaignById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateStaticVoucherCampaignByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate Static Vouchers Campaign
    ApiResponse<WTStaticVoucherCampaign> response = apiInstance.DuplicateStaticVoucherCampaignByIdWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.DuplicateStaticVoucherCampaignByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**WTStaticVoucherCampaign**](WTStaticVoucherCampaign.md)

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

<a id="fetchperformanceoverview"></a>
# **FetchPerformanceOverview**
> Object FetchPerformanceOverview (string campaignID)

Get Static Voucher Campaign performance overview

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
    public class FetchPerformanceOverviewExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Get Static Voucher Campaign performance overview
                Object result = apiInstance.FetchPerformanceOverview(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchPerformanceOverview: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchPerformanceOverviewWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Static Voucher Campaign performance overview
    ApiResponse<Object> response = apiInstance.FetchPerformanceOverviewWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchPerformanceOverviewWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

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

<a id="fetchreachstatsofallstaticvouchercampaigns"></a>
# **FetchReachStatsOfAllStaticVoucherCampaigns**
> ReachPerformanceStats FetchReachStatsOfAllStaticVoucherCampaigns (DateTime? broadcastScheduledStartAt = null, DateTime? broadcastScheduledEndAt = null)

Get the reach statistics of all Static Voucher Campaigns

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
    public class FetchReachStatsOfAllStaticVoucherCampaignsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var broadcastScheduledStartAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var broadcastScheduledEndAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get the reach statistics of all Static Voucher Campaigns
                ReachPerformanceStats result = apiInstance.FetchReachStatsOfAllStaticVoucherCampaigns(broadcastScheduledStartAt, broadcastScheduledEndAt);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchReachStatsOfAllStaticVoucherCampaigns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchReachStatsOfAllStaticVoucherCampaignsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get the reach statistics of all Static Voucher Campaigns
    ApiResponse<ReachPerformanceStats> response = apiInstance.FetchReachStatsOfAllStaticVoucherCampaignsWithHttpInfo(broadcastScheduledStartAt, broadcastScheduledEndAt);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchReachStatsOfAllStaticVoucherCampaignsWithHttpInfo: " + e.Message);
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

<a id="fetchreachstatsofindividualstaticvouchercampaign"></a>
# **FetchReachStatsOfIndividualStaticVoucherCampaign**
> ReachPerformanceStats FetchReachStatsOfIndividualStaticVoucherCampaign (string staticVoucherCampaignID, DateTime? broadcastScheduledStartAt = null, DateTime? broadcastScheduledEndAt = null)

Get the reach statistics of a single Static Voucher Campaign

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
    public class FetchReachStatsOfIndividualStaticVoucherCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var staticVoucherCampaignID = "staticVoucherCampaignID_example";  // string | 
            var broadcastScheduledStartAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var broadcastScheduledEndAt = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get the reach statistics of a single Static Voucher Campaign
                ReachPerformanceStats result = apiInstance.FetchReachStatsOfIndividualStaticVoucherCampaign(staticVoucherCampaignID, broadcastScheduledStartAt, broadcastScheduledEndAt);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchReachStatsOfIndividualStaticVoucherCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchReachStatsOfIndividualStaticVoucherCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get the reach statistics of a single Static Voucher Campaign
    ApiResponse<ReachPerformanceStats> response = apiInstance.FetchReachStatsOfIndividualStaticVoucherCampaignWithHttpInfo(staticVoucherCampaignID, broadcastScheduledStartAt, broadcastScheduledEndAt);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchReachStatsOfIndividualStaticVoucherCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **staticVoucherCampaignID** | **string** |  |  |
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

<a id="fetchstaticvouchercampaignbyid"></a>
# **FetchStaticVoucherCampaignById**
> WTStaticVoucherCampaign FetchStaticVoucherCampaignById (string id)

Get Static Vouchers Campaign

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
    public class FetchStaticVoucherCampaignByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Static Vouchers Campaign
                WTStaticVoucherCampaign result = apiInstance.FetchStaticVoucherCampaignById(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchStaticVoucherCampaignById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchStaticVoucherCampaignByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Static Vouchers Campaign
    ApiResponse<WTStaticVoucherCampaign> response = apiInstance.FetchStaticVoucherCampaignByIdWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchStaticVoucherCampaignByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTStaticVoucherCampaign**](WTStaticVoucherCampaign.md)

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

<a id="fetchstaticvouchercampaigns"></a>
# **FetchStaticVoucherCampaigns**
> List&lt;WTStaticVoucherCampaign&gt; FetchStaticVoucherCampaigns (bool? isArchiveIncluded = null, double? sourceID = null)

Get all Static Vouchers Campaigns

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
    public class FetchStaticVoucherCampaignsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 
            var sourceID = 1.2D;  // double? |  (optional) 

            try
            {
                // Get all Static Vouchers Campaigns
                List<WTStaticVoucherCampaign> result = apiInstance.FetchStaticVoucherCampaigns(isArchiveIncluded, sourceID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchStaticVoucherCampaigns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchStaticVoucherCampaignsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Static Vouchers Campaigns
    ApiResponse<List<WTStaticVoucherCampaign>> response = apiInstance.FetchStaticVoucherCampaignsWithHttpInfo(isArchiveIncluded, sourceID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchStaticVoucherCampaignsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |
| **sourceID** | **double?** |  | [optional]  |

### Return type

[**List&lt;WTStaticVoucherCampaign&gt;**](WTStaticVoucherCampaign.md)

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

<a id="fetchstaticvouchers"></a>
# **FetchStaticVouchers**
> List&lt;WTStaticVoucher&gt; FetchStaticVouchers (string campaignID)

Get vouchers in Static Vouchers Campaign

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
    public class FetchStaticVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Get vouchers in Static Vouchers Campaign
                List<WTStaticVoucher> result = apiInstance.FetchStaticVouchers(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchStaticVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchStaticVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get vouchers in Static Vouchers Campaign
    ApiResponse<List<WTStaticVoucher>> response = apiInstance.FetchStaticVouchersWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchStaticVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**List&lt;WTStaticVoucher&gt;**](WTStaticVoucher.md)

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

<a id="fetchstaticvoucherspage"></a>
# **FetchStaticVouchersPage**
> FetchStaticVouchersPage200Response FetchStaticVouchersPage (string campaignID, double pagenum, double pagesize)

Get a page of vouchers in a Static Voucher Campaign

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
    public class FetchStaticVouchersPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 
            var pagenum = 1.2D;  // double | 
            var pagesize = 1.2D;  // double | 

            try
            {
                // Get a page of vouchers in a Static Voucher Campaign
                FetchStaticVouchersPage200Response result = apiInstance.FetchStaticVouchersPage(campaignID, pagenum, pagesize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchStaticVouchersPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchStaticVouchersPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a page of vouchers in a Static Voucher Campaign
    ApiResponse<FetchStaticVouchersPage200Response> response = apiInstance.FetchStaticVouchersPageWithHttpInfo(campaignID, pagenum, pagesize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchStaticVouchersPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |
| **pagenum** | **double** |  |  |
| **pagesize** | **double** |  |  |

### Return type

[**FetchStaticVouchersPage200Response**](FetchStaticVouchersPage200Response.md)

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

<a id="fetchviews"></a>
# **FetchViews**
> List&lt;WTWalletPageView&gt; FetchViews (string campaignID)

Get Static Vouchers Campaign traffic

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
    public class FetchViewsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Get Static Vouchers Campaign traffic
                List<WTWalletPageView> result = apiInstance.FetchViews(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchViews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchViewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Static Vouchers Campaign traffic
    ApiResponse<List<WTWalletPageView>> response = apiInstance.FetchViewsWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchViewsWithHttpInfo: " + e.Message);
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

<a id="fetchvouchersredeemed"></a>
# **FetchVouchersRedeemed**
> List&lt;WTStaticVoucher&gt; FetchVouchersRedeemed (string campaignID)

Get redeemed vouchers in Static Vouchers Campaign

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
    public class FetchVouchersRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Get redeemed vouchers in Static Vouchers Campaign
                List<WTStaticVoucher> result = apiInstance.FetchVouchersRedeemed(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchVouchersRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchVouchersRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redeemed vouchers in Static Vouchers Campaign
    ApiResponse<List<WTStaticVoucher>> response = apiInstance.FetchVouchersRedeemedWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.FetchVouchersRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**List&lt;WTStaticVoucher&gt;**](WTStaticVoucher.md)

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

<a id="previewmessagesbypage"></a>
# **PreviewMessagesByPage**
> VSCampaignGeneratedMessagePagination PreviewMessagesByPage (string campaignID, WTStaticVoucherCampaignPreviewMessagesByPage wTStaticVoucherCampaignPreviewMessagesByPage)

Preview generated broadcast messages by page

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
    public class PreviewMessagesByPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 
            var wTStaticVoucherCampaignPreviewMessagesByPage = new WTStaticVoucherCampaignPreviewMessagesByPage(); // WTStaticVoucherCampaignPreviewMessagesByPage | 

            try
            {
                // Preview generated broadcast messages by page
                VSCampaignGeneratedMessagePagination result = apiInstance.PreviewMessagesByPage(campaignID, wTStaticVoucherCampaignPreviewMessagesByPage);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.PreviewMessagesByPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewMessagesByPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview generated broadcast messages by page
    ApiResponse<VSCampaignGeneratedMessagePagination> response = apiInstance.PreviewMessagesByPageWithHttpInfo(campaignID, wTStaticVoucherCampaignPreviewMessagesByPage);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.PreviewMessagesByPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |
| **wTStaticVoucherCampaignPreviewMessagesByPage** | [**WTStaticVoucherCampaignPreviewMessagesByPage**](WTStaticVoucherCampaignPreviewMessagesByPage.md) |  |  |

### Return type

[**VSCampaignGeneratedMessagePagination**](VSCampaignGeneratedMessagePagination.md)

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

<a id="restorestaticvouchercampaign"></a>
# **RestoreStaticVoucherCampaign**
> StaticVoucherCampaign RestoreStaticVoucherCampaign (string campaignID)

Restore Static Voucher Campaign

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
    public class RestoreStaticVoucherCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Restore Static Voucher Campaign
                StaticVoucherCampaign result = apiInstance.RestoreStaticVoucherCampaign(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.RestoreStaticVoucherCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreStaticVoucherCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Static Voucher Campaign
    ApiResponse<StaticVoucherCampaign> response = apiInstance.RestoreStaticVoucherCampaignWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.RestoreStaticVoucherCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

### Return type

[**StaticVoucherCampaign**](StaticVoucherCampaign.md)

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

<a id="updatestaticvouchercampaign"></a>
# **UpdateStaticVoucherCampaign**
> WTStaticVoucherCampaign UpdateStaticVoucherCampaign (string campaignID, StaticVoucherCampaignUpdate staticVoucherCampaignUpdate)

Update Static Voucher Campaign

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
    public class UpdateStaticVoucherCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 
            var staticVoucherCampaignUpdate = new StaticVoucherCampaignUpdate(); // StaticVoucherCampaignUpdate | 

            try
            {
                // Update Static Voucher Campaign
                WTStaticVoucherCampaign result = apiInstance.UpdateStaticVoucherCampaign(campaignID, staticVoucherCampaignUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.UpdateStaticVoucherCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateStaticVoucherCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Static Voucher Campaign
    ApiResponse<WTStaticVoucherCampaign> response = apiInstance.UpdateStaticVoucherCampaignWithHttpInfo(campaignID, staticVoucherCampaignUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.UpdateStaticVoucherCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |
| **staticVoucherCampaignUpdate** | [**StaticVoucherCampaignUpdate**](StaticVoucherCampaignUpdate.md) |  |  |

### Return type

[**WTStaticVoucherCampaign**](WTStaticVoucherCampaign.md)

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

<a id="updatestaticvouchercampaignwithvoucher"></a>
# **UpdateStaticVoucherCampaignWithVoucher**
> WTStaticVoucherCampaign UpdateStaticVoucherCampaignWithVoucher (string campaignID, UpdateStaticVoucherCampaignWithVoucher updateStaticVoucherCampaignWithVoucher)

Update Static Voucher Campaign with single voucher

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
    public class UpdateStaticVoucherCampaignWithVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new StaticVoucherCampaignsApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 
            var updateStaticVoucherCampaignWithVoucher = new UpdateStaticVoucherCampaignWithVoucher(); // UpdateStaticVoucherCampaignWithVoucher | 

            try
            {
                // Update Static Voucher Campaign with single voucher
                WTStaticVoucherCampaign result = apiInstance.UpdateStaticVoucherCampaignWithVoucher(campaignID, updateStaticVoucherCampaignWithVoucher);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaticVoucherCampaignsApi.UpdateStaticVoucherCampaignWithVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateStaticVoucherCampaignWithVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Static Voucher Campaign with single voucher
    ApiResponse<WTStaticVoucherCampaign> response = apiInstance.UpdateStaticVoucherCampaignWithVoucherWithHttpInfo(campaignID, updateStaticVoucherCampaignWithVoucher);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaticVoucherCampaignsApi.UpdateStaticVoucherCampaignWithVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |
| **updateStaticVoucherCampaignWithVoucher** | [**UpdateStaticVoucherCampaignWithVoucher**](UpdateStaticVoucherCampaignWithVoucher.md) |  |  |

### Return type

[**WTStaticVoucherCampaign**](WTStaticVoucherCampaign.md)

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

