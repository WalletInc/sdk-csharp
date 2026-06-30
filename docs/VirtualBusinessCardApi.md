# WalletInc.Api.VirtualBusinessCardApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveVirtualBusinessCard**](VirtualBusinessCardApi.md#archivevirtualbusinesscard) | **DELETE** /v2/virtualBusinessCard/{id} | Archive Virtual Business Card |
| [**CreateVirtualBusinessCard**](VirtualBusinessCardApi.md#createvirtualbusinesscard) | **POST** /v2/virtualBusinessCard | Create Virtual Business Card |
| [**FetchAllVirtualBusinessCards**](VirtualBusinessCardApi.md#fetchallvirtualbusinesscards) | **GET** /v2/virtualBusinessCard/all | Get all Virtual Business Cards |
| [**FetchVirtualBusinessCard**](VirtualBusinessCardApi.md#fetchvirtualbusinesscard) | **GET** /v2/virtualBusinessCard/{id} | Get Virtual Business Card |
| [**FetchVirtualBusinessCardRequests**](VirtualBusinessCardApi.md#fetchvirtualbusinesscardrequests) | **GET** /v2/virtualBusinessCard/requests/{id} | Get Virtual Business Card traffic |
| [**RestoreVirtualBusinessCard**](VirtualBusinessCardApi.md#restorevirtualbusinesscard) | **PATCH** /v2/virtualBusinessCard/{id} | Restore Virtual Business Card |
| [**UpdateVirtualBusinessCard**](VirtualBusinessCardApi.md#updatevirtualbusinesscard) | **PUT** /v2/virtualBusinessCard/{id} | Update Virtual Business Card |

<a id="archivevirtualbusinesscard"></a>
# **ArchiveVirtualBusinessCard**
> VirtualBusinessCard ArchiveVirtualBusinessCard (string id)

Archive Virtual Business Card

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
    public class ArchiveVirtualBusinessCardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new VirtualBusinessCardApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive Virtual Business Card
                VirtualBusinessCard result = apiInstance.ArchiveVirtualBusinessCard(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VirtualBusinessCardApi.ArchiveVirtualBusinessCard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveVirtualBusinessCardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Virtual Business Card
    ApiResponse<VirtualBusinessCard> response = apiInstance.ArchiveVirtualBusinessCardWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VirtualBusinessCardApi.ArchiveVirtualBusinessCardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**VirtualBusinessCard**](VirtualBusinessCard.md)

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

<a id="createvirtualbusinesscard"></a>
# **CreateVirtualBusinessCard**
> VirtualBusinessCard CreateVirtualBusinessCard (WTVirtualBusinessCardCreateParams wTVirtualBusinessCardCreateParams)

Create Virtual Business Card

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
    public class CreateVirtualBusinessCardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new VirtualBusinessCardApi(httpClient, config, httpClientHandler);
            var wTVirtualBusinessCardCreateParams = new WTVirtualBusinessCardCreateParams(); // WTVirtualBusinessCardCreateParams | 

            try
            {
                // Create Virtual Business Card
                VirtualBusinessCard result = apiInstance.CreateVirtualBusinessCard(wTVirtualBusinessCardCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VirtualBusinessCardApi.CreateVirtualBusinessCard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateVirtualBusinessCardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Virtual Business Card
    ApiResponse<VirtualBusinessCard> response = apiInstance.CreateVirtualBusinessCardWithHttpInfo(wTVirtualBusinessCardCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VirtualBusinessCardApi.CreateVirtualBusinessCardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTVirtualBusinessCardCreateParams** | [**WTVirtualBusinessCardCreateParams**](WTVirtualBusinessCardCreateParams.md) |  |  |

### Return type

[**VirtualBusinessCard**](VirtualBusinessCard.md)

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

<a id="fetchallvirtualbusinesscards"></a>
# **FetchAllVirtualBusinessCards**
> Object FetchAllVirtualBusinessCards (bool? isArchiveIncluded = null)

Get all Virtual Business Cards

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
    public class FetchAllVirtualBusinessCardsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new VirtualBusinessCardApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all Virtual Business Cards
                Object result = apiInstance.FetchAllVirtualBusinessCards(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VirtualBusinessCardApi.FetchAllVirtualBusinessCards: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllVirtualBusinessCardsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Virtual Business Cards
    ApiResponse<Object> response = apiInstance.FetchAllVirtualBusinessCardsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VirtualBusinessCardApi.FetchAllVirtualBusinessCardsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

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

<a id="fetchvirtualbusinesscard"></a>
# **FetchVirtualBusinessCard**
> VirtualBusinessCard FetchVirtualBusinessCard (string id)

Get Virtual Business Card

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
    public class FetchVirtualBusinessCardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new VirtualBusinessCardApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Virtual Business Card
                VirtualBusinessCard result = apiInstance.FetchVirtualBusinessCard(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VirtualBusinessCardApi.FetchVirtualBusinessCard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchVirtualBusinessCardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Virtual Business Card
    ApiResponse<VirtualBusinessCard> response = apiInstance.FetchVirtualBusinessCardWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VirtualBusinessCardApi.FetchVirtualBusinessCardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**VirtualBusinessCard**](VirtualBusinessCard.md)

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

<a id="fetchvirtualbusinesscardrequests"></a>
# **FetchVirtualBusinessCardRequests**
> List&lt;WalletPageView&gt; FetchVirtualBusinessCardRequests (string id)

Get Virtual Business Card traffic

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
    public class FetchVirtualBusinessCardRequestsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new VirtualBusinessCardApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Virtual Business Card traffic
                List<WalletPageView> result = apiInstance.FetchVirtualBusinessCardRequests(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VirtualBusinessCardApi.FetchVirtualBusinessCardRequests: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchVirtualBusinessCardRequestsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Virtual Business Card traffic
    ApiResponse<List<WalletPageView>> response = apiInstance.FetchVirtualBusinessCardRequestsWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VirtualBusinessCardApi.FetchVirtualBusinessCardRequestsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**List&lt;WalletPageView&gt;**](WalletPageView.md)

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

<a id="restorevirtualbusinesscard"></a>
# **RestoreVirtualBusinessCard**
> VirtualBusinessCard RestoreVirtualBusinessCard (string id)

Restore Virtual Business Card

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
    public class RestoreVirtualBusinessCardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new VirtualBusinessCardApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore Virtual Business Card
                VirtualBusinessCard result = apiInstance.RestoreVirtualBusinessCard(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VirtualBusinessCardApi.RestoreVirtualBusinessCard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreVirtualBusinessCardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Virtual Business Card
    ApiResponse<VirtualBusinessCard> response = apiInstance.RestoreVirtualBusinessCardWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VirtualBusinessCardApi.RestoreVirtualBusinessCardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**VirtualBusinessCard**](VirtualBusinessCard.md)

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

<a id="updatevirtualbusinesscard"></a>
# **UpdateVirtualBusinessCard**
> VirtualBusinessCard UpdateVirtualBusinessCard (string id, WTVirtualBusinessCardUpdateParams wTVirtualBusinessCardUpdateParams)

Update Virtual Business Card

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
    public class UpdateVirtualBusinessCardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new VirtualBusinessCardApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTVirtualBusinessCardUpdateParams = new WTVirtualBusinessCardUpdateParams(); // WTVirtualBusinessCardUpdateParams | 

            try
            {
                // Update Virtual Business Card
                VirtualBusinessCard result = apiInstance.UpdateVirtualBusinessCard(id, wTVirtualBusinessCardUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VirtualBusinessCardApi.UpdateVirtualBusinessCard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateVirtualBusinessCardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Virtual Business Card
    ApiResponse<VirtualBusinessCard> response = apiInstance.UpdateVirtualBusinessCardWithHttpInfo(id, wTVirtualBusinessCardUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VirtualBusinessCardApi.UpdateVirtualBusinessCardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTVirtualBusinessCardUpdateParams** | [**WTVirtualBusinessCardUpdateParams**](WTVirtualBusinessCardUpdateParams.md) |  |  |

### Return type

[**VirtualBusinessCard**](VirtualBusinessCard.md)

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

