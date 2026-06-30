# WalletInc.Api.MerchantCreditsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveMerchantCredit**](MerchantCreditsApi.md#archivemerchantcredit) | **DELETE** /v2/payment/merchantcredit/{id} | Archive Merchant Credit |
| [**CreateMerchantCredit**](MerchantCreditsApi.md#createmerchantcredit) | **POST** /v2/payment/merchantcredit | Create Merchant Credit |
| [**FetchMerchantCreditById**](MerchantCreditsApi.md#fetchmerchantcreditbyid) | **GET** /v2/payment/merchantcredit/{id} | Get Merchant Credit |
| [**FetchMerchantCreditCount**](MerchantCreditsApi.md#fetchmerchantcreditcount) | **GET** /v2/payment/merchantcredit/count | Count all Merchant Credits |
| [**FetchMerchantCreditHistoryLog**](MerchantCreditsApi.md#fetchmerchantcredithistorylog) | **POST** /v2/payment/merchantcredit/history/log | Get history |
| [**FetchMerchantCreditRedemptionLog**](MerchantCreditsApi.md#fetchmerchantcreditredemptionlog) | **POST** /v2/payment/merchantcredit/redemption/log | Get redemption log |
| [**FetchMerchantCreditsByPage**](MerchantCreditsApi.md#fetchmerchantcreditsbypage) | **POST** /v2/payment/merchantcredit/page | Get Merchant Credits |
| [**RestoreMerchantCredit**](MerchantCreditsApi.md#restoremerchantcredit) | **PATCH** /v2/payment/merchantcredit/{id} | Restore Merchant Credit |
| [**SearchMerchantCredits**](MerchantCreditsApi.md#searchmerchantcredits) | **POST** /v2/payment/merchantcredit/search | Search for Merchant Credits with Member ID |
| [**UpdateMerchantCredit**](MerchantCreditsApi.md#updatemerchantcredit) | **PUT** /v2/payment/merchantcredit/{id} | Update Merchant Credit |

<a id="archivemerchantcredit"></a>
# **ArchiveMerchantCredit**
> WTMerchantCredit ArchiveMerchantCredit (string id)

Archive Merchant Credit

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
    public class ArchiveMerchantCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive Merchant Credit
                WTMerchantCredit result = apiInstance.ArchiveMerchantCredit(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.ArchiveMerchantCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveMerchantCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Merchant Credit
    ApiResponse<WTMerchantCredit> response = apiInstance.ArchiveMerchantCreditWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.ArchiveMerchantCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTMerchantCredit**](WTMerchantCredit.md)

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

<a id="createmerchantcredit"></a>
# **CreateMerchantCredit**
> WTMerchantCredit CreateMerchantCredit (WTMerchantCreditCreationParams wTMerchantCreditCreationParams)

Create Merchant Credit

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
    public class CreateMerchantCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var wTMerchantCreditCreationParams = new WTMerchantCreditCreationParams(); // WTMerchantCreditCreationParams | 

            try
            {
                // Create Merchant Credit
                WTMerchantCredit result = apiInstance.CreateMerchantCredit(wTMerchantCreditCreationParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.CreateMerchantCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateMerchantCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Merchant Credit
    ApiResponse<WTMerchantCredit> response = apiInstance.CreateMerchantCreditWithHttpInfo(wTMerchantCreditCreationParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.CreateMerchantCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMerchantCreditCreationParams** | [**WTMerchantCreditCreationParams**](WTMerchantCreditCreationParams.md) |  |  |

### Return type

[**WTMerchantCredit**](WTMerchantCredit.md)

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

<a id="fetchmerchantcreditbyid"></a>
# **FetchMerchantCreditById**
> WTMerchantCredit FetchMerchantCreditById (string id)

Get Merchant Credit

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
    public class FetchMerchantCreditByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Merchant Credit
                WTMerchantCredit result = apiInstance.FetchMerchantCreditById(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMerchantCreditByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Merchant Credit
    ApiResponse<WTMerchantCredit> response = apiInstance.FetchMerchantCreditByIdWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTMerchantCredit**](WTMerchantCredit.md)

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

<a id="fetchmerchantcreditcount"></a>
# **FetchMerchantCreditCount**
> FetchMembersCount200Response FetchMerchantCreditCount ()

Count all Merchant Credits

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
    public class FetchMerchantCreditCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);

            try
            {
                // Count all Merchant Credits
                FetchMembersCount200Response result = apiInstance.FetchMerchantCreditCount();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMerchantCreditCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count all Merchant Credits
    ApiResponse<FetchMembersCount200Response> response = apiInstance.FetchMerchantCreditCountWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
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

<a id="fetchmerchantcredithistorylog"></a>
# **FetchMerchantCreditHistoryLog**
> MSMerchantCreditHistoryPagination FetchMerchantCreditHistoryLog (PaginationRequestWithIDAndWithoutSortOptions paginationRequestWithIDAndWithoutSortOptions)

Get history

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
    public class FetchMerchantCreditHistoryLogExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var paginationRequestWithIDAndWithoutSortOptions = new PaginationRequestWithIDAndWithoutSortOptions(); // PaginationRequestWithIDAndWithoutSortOptions | 

            try
            {
                // Get history
                MSMerchantCreditHistoryPagination result = apiInstance.FetchMerchantCreditHistoryLog(paginationRequestWithIDAndWithoutSortOptions);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditHistoryLog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMerchantCreditHistoryLogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get history
    ApiResponse<MSMerchantCreditHistoryPagination> response = apiInstance.FetchMerchantCreditHistoryLogWithHttpInfo(paginationRequestWithIDAndWithoutSortOptions);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditHistoryLogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paginationRequestWithIDAndWithoutSortOptions** | [**PaginationRequestWithIDAndWithoutSortOptions**](PaginationRequestWithIDAndWithoutSortOptions.md) |  |  |

### Return type

[**MSMerchantCreditHistoryPagination**](MSMerchantCreditHistoryPagination.md)

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

<a id="fetchmerchantcreditredemptionlog"></a>
# **FetchMerchantCreditRedemptionLog**
> MSMerchantCreditRedemptionPagination FetchMerchantCreditRedemptionLog (PaginationRequestWithIDAndWithoutSortOptions paginationRequestWithIDAndWithoutSortOptions)

Get redemption log

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
    public class FetchMerchantCreditRedemptionLogExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var paginationRequestWithIDAndWithoutSortOptions = new PaginationRequestWithIDAndWithoutSortOptions(); // PaginationRequestWithIDAndWithoutSortOptions | 

            try
            {
                // Get redemption log
                MSMerchantCreditRedemptionPagination result = apiInstance.FetchMerchantCreditRedemptionLog(paginationRequestWithIDAndWithoutSortOptions);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditRedemptionLog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMerchantCreditRedemptionLogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redemption log
    ApiResponse<MSMerchantCreditRedemptionPagination> response = apiInstance.FetchMerchantCreditRedemptionLogWithHttpInfo(paginationRequestWithIDAndWithoutSortOptions);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditRedemptionLogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paginationRequestWithIDAndWithoutSortOptions** | [**PaginationRequestWithIDAndWithoutSortOptions**](PaginationRequestWithIDAndWithoutSortOptions.md) |  |  |

### Return type

[**MSMerchantCreditRedemptionPagination**](MSMerchantCreditRedemptionPagination.md)

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

<a id="fetchmerchantcreditsbypage"></a>
# **FetchMerchantCreditsByPage**
> List&lt;WTMerchantCredit&gt; FetchMerchantCreditsByPage (PaginationRequestWithSortOptions paginationRequestWithSortOptions)

Get Merchant Credits

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
    public class FetchMerchantCreditsByPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var paginationRequestWithSortOptions = new PaginationRequestWithSortOptions(); // PaginationRequestWithSortOptions | 

            try
            {
                // Get Merchant Credits
                List<WTMerchantCredit> result = apiInstance.FetchMerchantCreditsByPage(paginationRequestWithSortOptions);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditsByPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMerchantCreditsByPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Merchant Credits
    ApiResponse<List<WTMerchantCredit>> response = apiInstance.FetchMerchantCreditsByPageWithHttpInfo(paginationRequestWithSortOptions);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.FetchMerchantCreditsByPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paginationRequestWithSortOptions** | [**PaginationRequestWithSortOptions**](PaginationRequestWithSortOptions.md) |  |  |

### Return type

[**List&lt;WTMerchantCredit&gt;**](WTMerchantCredit.md)

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

<a id="restoremerchantcredit"></a>
# **RestoreMerchantCredit**
> WTMerchantCredit RestoreMerchantCredit (string id)

Restore Merchant Credit

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
    public class RestoreMerchantCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore Merchant Credit
                WTMerchantCredit result = apiInstance.RestoreMerchantCredit(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.RestoreMerchantCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreMerchantCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Merchant Credit
    ApiResponse<WTMerchantCredit> response = apiInstance.RestoreMerchantCreditWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.RestoreMerchantCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTMerchantCredit**](WTMerchantCredit.md)

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

<a id="searchmerchantcredits"></a>
# **SearchMerchantCredits**
> PaginatedWTMerchantCredits SearchMerchantCredits (MerchantCreditSearch merchantCreditSearch)

Search for Merchant Credits with Member ID

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
    public class SearchMerchantCreditsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var merchantCreditSearch = new MerchantCreditSearch(); // MerchantCreditSearch | 

            try
            {
                // Search for Merchant Credits with Member ID
                PaginatedWTMerchantCredits result = apiInstance.SearchMerchantCredits(merchantCreditSearch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.SearchMerchantCredits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchMerchantCreditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search for Merchant Credits with Member ID
    ApiResponse<PaginatedWTMerchantCredits> response = apiInstance.SearchMerchantCreditsWithHttpInfo(merchantCreditSearch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.SearchMerchantCreditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **merchantCreditSearch** | [**MerchantCreditSearch**](MerchantCreditSearch.md) |  |  |

### Return type

[**PaginatedWTMerchantCredits**](PaginatedWTMerchantCredits.md)

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

<a id="updatemerchantcredit"></a>
# **UpdateMerchantCredit**
> WTMerchantCredit UpdateMerchantCredit (string id, PickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber pickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber)

Update Merchant Credit

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
    public class UpdateMerchantCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantCreditsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var pickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber = new PickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber(); // PickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber | 

            try
            {
                // Update Merchant Credit
                WTMerchantCredit result = apiInstance.UpdateMerchantCredit(id, pickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantCreditsApi.UpdateMerchantCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateMerchantCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Merchant Credit
    ApiResponse<WTMerchantCredit> response = apiInstance.UpdateMerchantCreditWithHttpInfo(id, pickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantCreditsApi.UpdateMerchantCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **pickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber** | [**PickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber**](PickWTMerchantCreditMemberIDOrCreditAmountOrMobileNumber.md) |  |  |

### Return type

[**WTMerchantCredit**](WTMerchantCredit.md)

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

