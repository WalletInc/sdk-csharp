# WalletInc.Api.QuickLinksSectionApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveLinkBookSection**](QuickLinksSectionApi.md#archivelinkbooksection) | **DELETE** /v2/linkBookSection/{id} | Archive quick link section |
| [**CreateLinkBookSection**](QuickLinksSectionApi.md#createlinkbooksection) | **POST** /v2/linkBookSection | Create quick link section |
| [**FetchAllLinkBookSections**](QuickLinksSectionApi.md#fetchalllinkbooksections) | **GET** /v2/linkBookSection/all | Get all quick link sections |
| [**RestoreLinkBookSection**](QuickLinksSectionApi.md#restorelinkbooksection) | **PATCH** /v2/linkBookSection/{id} | Restore quick link section |
| [**UpdateLinkBookSection**](QuickLinksSectionApi.md#updatelinkbooksection) | **PUT** /v2/linkBookSection/{id} | Update quick link section |

<a id="archivelinkbooksection"></a>
# **ArchiveLinkBookSection**
> LinkBookSection ArchiveLinkBookSection (string id)

Archive quick link section

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
    public class ArchiveLinkBookSectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QuickLinksSectionApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive quick link section
                LinkBookSection result = apiInstance.ArchiveLinkBookSection(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuickLinksSectionApi.ArchiveLinkBookSection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveLinkBookSectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive quick link section
    ApiResponse<LinkBookSection> response = apiInstance.ArchiveLinkBookSectionWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuickLinksSectionApi.ArchiveLinkBookSectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**LinkBookSection**](LinkBookSection.md)

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

<a id="createlinkbooksection"></a>
# **CreateLinkBookSection**
> LinkBookSection CreateLinkBookSection (WTQuickLinkSectionCreateParams wTQuickLinkSectionCreateParams)

Create quick link section

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
    public class CreateLinkBookSectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QuickLinksSectionApi(httpClient, config, httpClientHandler);
            var wTQuickLinkSectionCreateParams = new WTQuickLinkSectionCreateParams(); // WTQuickLinkSectionCreateParams | 

            try
            {
                // Create quick link section
                LinkBookSection result = apiInstance.CreateLinkBookSection(wTQuickLinkSectionCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuickLinksSectionApi.CreateLinkBookSection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateLinkBookSectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create quick link section
    ApiResponse<LinkBookSection> response = apiInstance.CreateLinkBookSectionWithHttpInfo(wTQuickLinkSectionCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuickLinksSectionApi.CreateLinkBookSectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTQuickLinkSectionCreateParams** | [**WTQuickLinkSectionCreateParams**](WTQuickLinkSectionCreateParams.md) |  |  |

### Return type

[**LinkBookSection**](LinkBookSection.md)

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

<a id="fetchalllinkbooksections"></a>
# **FetchAllLinkBookSections**
> Object FetchAllLinkBookSections (bool? isArchiveIncluded = null)

Get all quick link sections

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
    public class FetchAllLinkBookSectionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QuickLinksSectionApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all quick link sections
                Object result = apiInstance.FetchAllLinkBookSections(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuickLinksSectionApi.FetchAllLinkBookSections: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllLinkBookSectionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all quick link sections
    ApiResponse<Object> response = apiInstance.FetchAllLinkBookSectionsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuickLinksSectionApi.FetchAllLinkBookSectionsWithHttpInfo: " + e.Message);
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

<a id="restorelinkbooksection"></a>
# **RestoreLinkBookSection**
> LinkBookSection RestoreLinkBookSection (string id)

Restore quick link section

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
    public class RestoreLinkBookSectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QuickLinksSectionApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore quick link section
                LinkBookSection result = apiInstance.RestoreLinkBookSection(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuickLinksSectionApi.RestoreLinkBookSection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreLinkBookSectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore quick link section
    ApiResponse<LinkBookSection> response = apiInstance.RestoreLinkBookSectionWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuickLinksSectionApi.RestoreLinkBookSectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**LinkBookSection**](LinkBookSection.md)

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

<a id="updatelinkbooksection"></a>
# **UpdateLinkBookSection**
> LinkBookSection UpdateLinkBookSection (string id, WTQuickLinkSectionUpdateParams wTQuickLinkSectionUpdateParams)

Update quick link section

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
    public class UpdateLinkBookSectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QuickLinksSectionApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTQuickLinkSectionUpdateParams = new WTQuickLinkSectionUpdateParams(); // WTQuickLinkSectionUpdateParams | 

            try
            {
                // Update quick link section
                LinkBookSection result = apiInstance.UpdateLinkBookSection(id, wTQuickLinkSectionUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuickLinksSectionApi.UpdateLinkBookSection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateLinkBookSectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update quick link section
    ApiResponse<LinkBookSection> response = apiInstance.UpdateLinkBookSectionWithHttpInfo(id, wTQuickLinkSectionUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuickLinksSectionApi.UpdateLinkBookSectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTQuickLinkSectionUpdateParams** | [**WTQuickLinkSectionUpdateParams**](WTQuickLinkSectionUpdateParams.md) |  |  |

### Return type

[**LinkBookSection**](LinkBookSection.md)

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

