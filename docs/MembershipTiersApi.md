# WalletInc.Api.MembershipTiersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveMembershipTier**](MembershipTiersApi.md#archivemembershiptier) | **DELETE** /v2/membership/tier/{id} | Archive Membership Tier |
| [**CreateMembershipTier**](MembershipTiersApi.md#createmembershiptier) | **POST** /v2/membership/tier | Create Membership Tier |
| [**FetchAllMembershipTiers**](MembershipTiersApi.md#fetchallmembershiptiers) | **GET** /v2/membership/tier/all | Get all Membership Tiers |
| [**FetchAllMembershipTiersWithMemberCount**](MembershipTiersApi.md#fetchallmembershiptierswithmembercount) | **GET** /v2/membership/tier/allWithMemberCount | Get all Membership Tiers with member count |
| [**FetchMembershipTierById**](MembershipTiersApi.md#fetchmembershiptierbyid) | **GET** /v2/membership/tier/{id} | Get Membership Tier |
| [**FetchMembershipTierHistoryLog**](MembershipTiersApi.md#fetchmembershiptierhistorylog) | **POST** /v2/membership/tier/history/log | Get Membership Tier history |
| [**FetchMembershipTierRedemptionLog**](MembershipTiersApi.md#fetchmembershiptierredemptionlog) | **POST** /v2/membership/tier/redemption/log | Get Membership Tier redemption log |
| [**RestoreMembershipTier**](MembershipTiersApi.md#restoremembershiptier) | **PATCH** /v2/membership/tier/{id} | Restore Membership Tier |
| [**UpdateMembershipTier**](MembershipTiersApi.md#updatemembershiptier) | **PUT** /v2/membership/tier/{id} | Update Membership Tier |

<a id="archivemembershiptier"></a>
# **ArchiveMembershipTier**
> WTMembershipTier ArchiveMembershipTier (string id)

Archive Membership Tier

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
    public class ArchiveMembershipTierExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive Membership Tier
                WTMembershipTier result = apiInstance.ArchiveMembershipTier(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.ArchiveMembershipTier: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveMembershipTierWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Membership Tier
    ApiResponse<WTMembershipTier> response = apiInstance.ArchiveMembershipTierWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.ArchiveMembershipTierWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTMembershipTier**](WTMembershipTier.md)

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

<a id="createmembershiptier"></a>
# **CreateMembershipTier**
> WTMembershipTier CreateMembershipTier (WTMembershipTierCreationParams wTMembershipTierCreationParams)

Create Membership Tier

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
    public class CreateMembershipTierExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var wTMembershipTierCreationParams = new WTMembershipTierCreationParams(); // WTMembershipTierCreationParams | 

            try
            {
                // Create Membership Tier
                WTMembershipTier result = apiInstance.CreateMembershipTier(wTMembershipTierCreationParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.CreateMembershipTier: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateMembershipTierWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Membership Tier
    ApiResponse<WTMembershipTier> response = apiInstance.CreateMembershipTierWithHttpInfo(wTMembershipTierCreationParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.CreateMembershipTierWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMembershipTierCreationParams** | [**WTMembershipTierCreationParams**](WTMembershipTierCreationParams.md) |  |  |

### Return type

[**WTMembershipTier**](WTMembershipTier.md)

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

<a id="fetchallmembershiptiers"></a>
# **FetchAllMembershipTiers**
> List&lt;WTMembershipTier&gt; FetchAllMembershipTiers (bool? isArchiveIncluded = null)

Get all Membership Tiers

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
    public class FetchAllMembershipTiersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all Membership Tiers
                List<WTMembershipTier> result = apiInstance.FetchAllMembershipTiers(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.FetchAllMembershipTiers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllMembershipTiersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Membership Tiers
    ApiResponse<List<WTMembershipTier>> response = apiInstance.FetchAllMembershipTiersWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.FetchAllMembershipTiersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;WTMembershipTier&gt;**](WTMembershipTier.md)

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

<a id="fetchallmembershiptierswithmembercount"></a>
# **FetchAllMembershipTiersWithMemberCount**
> List&lt;WTMembershipTierWithMemberCount&gt; FetchAllMembershipTiersWithMemberCount (bool? isArchiveIncluded = null)

Get all Membership Tiers with member count

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
    public class FetchAllMembershipTiersWithMemberCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all Membership Tiers with member count
                List<WTMembershipTierWithMemberCount> result = apiInstance.FetchAllMembershipTiersWithMemberCount(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.FetchAllMembershipTiersWithMemberCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllMembershipTiersWithMemberCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Membership Tiers with member count
    ApiResponse<List<WTMembershipTierWithMemberCount>> response = apiInstance.FetchAllMembershipTiersWithMemberCountWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.FetchAllMembershipTiersWithMemberCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;WTMembershipTierWithMemberCount&gt;**](WTMembershipTierWithMemberCount.md)

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

<a id="fetchmembershiptierbyid"></a>
# **FetchMembershipTierById**
> WTMembershipTier FetchMembershipTierById (string id)

Get Membership Tier

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
    public class FetchMembershipTierByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Membership Tier
                WTMembershipTier result = apiInstance.FetchMembershipTierById(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.FetchMembershipTierById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMembershipTierByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Membership Tier
    ApiResponse<WTMembershipTier> response = apiInstance.FetchMembershipTierByIdWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.FetchMembershipTierByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTMembershipTier**](WTMembershipTier.md)

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

<a id="fetchmembershiptierhistorylog"></a>
# **FetchMembershipTierHistoryLog**
> MSMembershipTierHistoryPagination FetchMembershipTierHistoryLog (PaginationRequestWithIDAndWithoutSortOptions paginationRequestWithIDAndWithoutSortOptions)

Get Membership Tier history

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
    public class FetchMembershipTierHistoryLogExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var paginationRequestWithIDAndWithoutSortOptions = new PaginationRequestWithIDAndWithoutSortOptions(); // PaginationRequestWithIDAndWithoutSortOptions | 

            try
            {
                // Get Membership Tier history
                MSMembershipTierHistoryPagination result = apiInstance.FetchMembershipTierHistoryLog(paginationRequestWithIDAndWithoutSortOptions);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.FetchMembershipTierHistoryLog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMembershipTierHistoryLogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Membership Tier history
    ApiResponse<MSMembershipTierHistoryPagination> response = apiInstance.FetchMembershipTierHistoryLogWithHttpInfo(paginationRequestWithIDAndWithoutSortOptions);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.FetchMembershipTierHistoryLogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paginationRequestWithIDAndWithoutSortOptions** | [**PaginationRequestWithIDAndWithoutSortOptions**](PaginationRequestWithIDAndWithoutSortOptions.md) |  |  |

### Return type

[**MSMembershipTierHistoryPagination**](MSMembershipTierHistoryPagination.md)

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

<a id="fetchmembershiptierredemptionlog"></a>
# **FetchMembershipTierRedemptionLog**
> MSMembershipTierRedemptionPagination FetchMembershipTierRedemptionLog (PaginationRequestWithIDAndWithoutSortOptions paginationRequestWithIDAndWithoutSortOptions)

Get Membership Tier redemption log

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
    public class FetchMembershipTierRedemptionLogExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var paginationRequestWithIDAndWithoutSortOptions = new PaginationRequestWithIDAndWithoutSortOptions(); // PaginationRequestWithIDAndWithoutSortOptions | 

            try
            {
                // Get Membership Tier redemption log
                MSMembershipTierRedemptionPagination result = apiInstance.FetchMembershipTierRedemptionLog(paginationRequestWithIDAndWithoutSortOptions);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.FetchMembershipTierRedemptionLog: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMembershipTierRedemptionLogWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Membership Tier redemption log
    ApiResponse<MSMembershipTierRedemptionPagination> response = apiInstance.FetchMembershipTierRedemptionLogWithHttpInfo(paginationRequestWithIDAndWithoutSortOptions);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.FetchMembershipTierRedemptionLogWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paginationRequestWithIDAndWithoutSortOptions** | [**PaginationRequestWithIDAndWithoutSortOptions**](PaginationRequestWithIDAndWithoutSortOptions.md) |  |  |

### Return type

[**MSMembershipTierRedemptionPagination**](MSMembershipTierRedemptionPagination.md)

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

<a id="restoremembershiptier"></a>
# **RestoreMembershipTier**
> WTMembershipTier RestoreMembershipTier (string id)

Restore Membership Tier

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
    public class RestoreMembershipTierExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore Membership Tier
                WTMembershipTier result = apiInstance.RestoreMembershipTier(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.RestoreMembershipTier: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreMembershipTierWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Membership Tier
    ApiResponse<WTMembershipTier> response = apiInstance.RestoreMembershipTierWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.RestoreMembershipTierWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTMembershipTier**](WTMembershipTier.md)

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

<a id="updatemembershiptier"></a>
# **UpdateMembershipTier**
> WTMembershipTier UpdateMembershipTier (string id, WTMembershipTierUpdateParams wTMembershipTierUpdateParams)

Update Membership Tier

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
    public class UpdateMembershipTierExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MembershipTiersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTMembershipTierUpdateParams = new WTMembershipTierUpdateParams(); // WTMembershipTierUpdateParams | 

            try
            {
                // Update Membership Tier
                WTMembershipTier result = apiInstance.UpdateMembershipTier(id, wTMembershipTierUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MembershipTiersApi.UpdateMembershipTier: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateMembershipTierWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Membership Tier
    ApiResponse<WTMembershipTier> response = apiInstance.UpdateMembershipTierWithHttpInfo(id, wTMembershipTierUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MembershipTiersApi.UpdateMembershipTierWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTMembershipTierUpdateParams** | [**WTMembershipTierUpdateParams**](WTMembershipTierUpdateParams.md) |  |  |

### Return type

[**WTMembershipTier**](WTMembershipTier.md)

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

