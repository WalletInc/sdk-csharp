# WalletInc.Api.RelatedItemsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchRelatedItemUsage**](RelatedItemsApi.md#fetchrelateditemusage) | **GET** /relatedItems/usedBy/{type}/{id} | List where an item is attached |
| [**FetchRelatedItems**](RelatedItemsApi.md#fetchrelateditems) | **GET** /relatedItems/{type}/{id} | Get an item&#39;s related items |
| [**SaveRelatedItems**](RelatedItemsApi.md#saverelateditems) | **PUT** /relatedItems/{type}/{id} | Set an item&#39;s related items |
| [**SearchRelatedItems**](RelatedItemsApi.md#searchrelateditems) | **GET** /relatedItems/search | Search items to attach |

<a id="fetchrelateditemusage"></a>
# **FetchRelatedItemUsage**
> List&lt;WTRelatedItemUsage&gt; FetchRelatedItemUsage (WTRelatedItemType type, string id)

List where an item is attached

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
    public class FetchRelatedItemUsageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new RelatedItemsApi(httpClient, config, httpClientHandler);
            var type = (WTRelatedItemType) "product";  // WTRelatedItemType | 
            var id = "id_example";  // string | 

            try
            {
                // List where an item is attached
                List<WTRelatedItemUsage> result = apiInstance.FetchRelatedItemUsage(type, id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RelatedItemsApi.FetchRelatedItemUsage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchRelatedItemUsageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List where an item is attached
    ApiResponse<List<WTRelatedItemUsage>> response = apiInstance.FetchRelatedItemUsageWithHttpInfo(type, id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RelatedItemsApi.FetchRelatedItemUsageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **type** | **WTRelatedItemType** |  |  |
| **id** | **string** |  |  |

### Return type

[**List&lt;WTRelatedItemUsage&gt;**](WTRelatedItemUsage.md)

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

<a id="fetchrelateditems"></a>
# **FetchRelatedItems**
> WTRelatedItems FetchRelatedItems (WTRelatedItemSourceType type, string id)

Get an item's related items

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
    public class FetchRelatedItemsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new RelatedItemsApi(httpClient, config, httpClientHandler);
            var type = (WTRelatedItemSourceType) "product";  // WTRelatedItemSourceType | 
            var id = "id_example";  // string | 

            try
            {
                // Get an item's related items
                WTRelatedItems result = apiInstance.FetchRelatedItems(type, id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RelatedItemsApi.FetchRelatedItems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchRelatedItemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an item's related items
    ApiResponse<WTRelatedItems> response = apiInstance.FetchRelatedItemsWithHttpInfo(type, id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RelatedItemsApi.FetchRelatedItemsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **type** | **WTRelatedItemSourceType** |  |  |
| **id** | **string** |  |  |

### Return type

[**WTRelatedItems**](WTRelatedItems.md)

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

<a id="saverelateditems"></a>
# **SaveRelatedItems**
> WTRelatedItems SaveRelatedItems (WTRelatedItemSourceType type, string id, WTRelatedItemsUpdate wTRelatedItemsUpdate)

Set an item's related items

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
    public class SaveRelatedItemsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new RelatedItemsApi(httpClient, config, httpClientHandler);
            var type = (WTRelatedItemSourceType) "product";  // WTRelatedItemSourceType | 
            var id = "id_example";  // string | 
            var wTRelatedItemsUpdate = new WTRelatedItemsUpdate(); // WTRelatedItemsUpdate | 

            try
            {
                // Set an item's related items
                WTRelatedItems result = apiInstance.SaveRelatedItems(type, id, wTRelatedItemsUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RelatedItemsApi.SaveRelatedItems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveRelatedItemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set an item's related items
    ApiResponse<WTRelatedItems> response = apiInstance.SaveRelatedItemsWithHttpInfo(type, id, wTRelatedItemsUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RelatedItemsApi.SaveRelatedItemsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **type** | **WTRelatedItemSourceType** |  |  |
| **id** | **string** |  |  |
| **wTRelatedItemsUpdate** | [**WTRelatedItemsUpdate**](WTRelatedItemsUpdate.md) |  |  |

### Return type

[**WTRelatedItems**](WTRelatedItems.md)

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

<a id="searchrelateditems"></a>
# **SearchRelatedItems**
> WTRelatedItemSearchResults SearchRelatedItems (string? q = null, WTRelatedItemType? type = null, double? page = null)

Search items to attach

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
    public class SearchRelatedItemsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new RelatedItemsApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string? |  (optional) 
            var type = new WTRelatedItemType?(); // WTRelatedItemType? |  (optional) 
            var page = 1.2D;  // double? |  (optional) 

            try
            {
                // Search items to attach
                WTRelatedItemSearchResults result = apiInstance.SearchRelatedItems(q, type, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RelatedItemsApi.SearchRelatedItems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchRelatedItemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search items to attach
    ApiResponse<WTRelatedItemSearchResults> response = apiInstance.SearchRelatedItemsWithHttpInfo(q, type, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RelatedItemsApi.SearchRelatedItemsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string?** |  | [optional]  |
| **type** | [**WTRelatedItemType?**](WTRelatedItemType?.md) |  | [optional]  |
| **page** | **double?** |  | [optional]  |

### Return type

[**WTRelatedItemSearchResults**](WTRelatedItemSearchResults.md)

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

