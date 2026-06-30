# WalletInc.Api.QRCodeDesignsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveQRCodeDesign**](QRCodeDesignsApi.md#archiveqrcodedesign) | **DELETE** /v2/qrcodedesign/{id} | Archive QR Code Design |
| [**CreateQRCodeDesign**](QRCodeDesignsApi.md#createqrcodedesign) | **POST** /v2/qrcodedesign | Create QR Code design |
| [**FetchAllQRCodeDesigns**](QRCodeDesignsApi.md#fetchallqrcodedesigns) | **GET** /v2/qrcodedesign/all | Get all QR Code Designs |
| [**FetchQRCodeDesignById**](QRCodeDesignsApi.md#fetchqrcodedesignbyid) | **GET** /v2/qrcodedesign/{id} | Get QR Code Design |
| [**RestoreQRCodeDesign**](QRCodeDesignsApi.md#restoreqrcodedesign) | **PATCH** /v2/qrcodedesign/{id} | Restore QR Code Design |
| [**UpdateQRCodeDesign**](QRCodeDesignsApi.md#updateqrcodedesign) | **PUT** /v2/qrcodedesign/{id} | Update QR Code Design |

<a id="archiveqrcodedesign"></a>
# **ArchiveQRCodeDesign**
> WTQRCodeDesign ArchiveQRCodeDesign (string id)

Archive QR Code Design

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
    public class ArchiveQRCodeDesignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QRCodeDesignsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive QR Code Design
                WTQRCodeDesign result = apiInstance.ArchiveQRCodeDesign(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QRCodeDesignsApi.ArchiveQRCodeDesign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveQRCodeDesignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive QR Code Design
    ApiResponse<WTQRCodeDesign> response = apiInstance.ArchiveQRCodeDesignWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QRCodeDesignsApi.ArchiveQRCodeDesignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTQRCodeDesign**](WTQRCodeDesign.md)

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

<a id="createqrcodedesign"></a>
# **CreateQRCodeDesign**
> WTQRCodeDesign CreateQRCodeDesign (WTQRCodeDesignCreateParams wTQRCodeDesignCreateParams)

Create QR Code design

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
    public class CreateQRCodeDesignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QRCodeDesignsApi(httpClient, config, httpClientHandler);
            var wTQRCodeDesignCreateParams = new WTQRCodeDesignCreateParams(); // WTQRCodeDesignCreateParams | 

            try
            {
                // Create QR Code design
                WTQRCodeDesign result = apiInstance.CreateQRCodeDesign(wTQRCodeDesignCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QRCodeDesignsApi.CreateQRCodeDesign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateQRCodeDesignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create QR Code design
    ApiResponse<WTQRCodeDesign> response = apiInstance.CreateQRCodeDesignWithHttpInfo(wTQRCodeDesignCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QRCodeDesignsApi.CreateQRCodeDesignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTQRCodeDesignCreateParams** | [**WTQRCodeDesignCreateParams**](WTQRCodeDesignCreateParams.md) |  |  |

### Return type

[**WTQRCodeDesign**](WTQRCodeDesign.md)

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

<a id="fetchallqrcodedesigns"></a>
# **FetchAllQRCodeDesigns**
> List&lt;WTQRCodeDesign&gt; FetchAllQRCodeDesigns (bool? isArchiveIncluded = null)

Get all QR Code Designs

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
    public class FetchAllQRCodeDesignsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QRCodeDesignsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all QR Code Designs
                List<WTQRCodeDesign> result = apiInstance.FetchAllQRCodeDesigns(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QRCodeDesignsApi.FetchAllQRCodeDesigns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllQRCodeDesignsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all QR Code Designs
    ApiResponse<List<WTQRCodeDesign>> response = apiInstance.FetchAllQRCodeDesignsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QRCodeDesignsApi.FetchAllQRCodeDesignsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;WTQRCodeDesign&gt;**](WTQRCodeDesign.md)

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

<a id="fetchqrcodedesignbyid"></a>
# **FetchQRCodeDesignById**
> WTQRCodeDesign FetchQRCodeDesignById (string id)

Get QR Code Design

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
    public class FetchQRCodeDesignByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QRCodeDesignsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get QR Code Design
                WTQRCodeDesign result = apiInstance.FetchQRCodeDesignById(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QRCodeDesignsApi.FetchQRCodeDesignById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchQRCodeDesignByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get QR Code Design
    ApiResponse<WTQRCodeDesign> response = apiInstance.FetchQRCodeDesignByIdWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QRCodeDesignsApi.FetchQRCodeDesignByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTQRCodeDesign**](WTQRCodeDesign.md)

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

<a id="restoreqrcodedesign"></a>
# **RestoreQRCodeDesign**
> QRCodeDesign RestoreQRCodeDesign (string id)

Restore QR Code Design

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
    public class RestoreQRCodeDesignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QRCodeDesignsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore QR Code Design
                QRCodeDesign result = apiInstance.RestoreQRCodeDesign(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QRCodeDesignsApi.RestoreQRCodeDesign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreQRCodeDesignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore QR Code Design
    ApiResponse<QRCodeDesign> response = apiInstance.RestoreQRCodeDesignWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QRCodeDesignsApi.RestoreQRCodeDesignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**QRCodeDesign**](QRCodeDesign.md)

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

<a id="updateqrcodedesign"></a>
# **UpdateQRCodeDesign**
> WTQRCodeDesign UpdateQRCodeDesign (string id, WTQRCodeDesignUpdateParams wTQRCodeDesignUpdateParams)

Update QR Code Design

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
    public class UpdateQRCodeDesignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new QRCodeDesignsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTQRCodeDesignUpdateParams = new WTQRCodeDesignUpdateParams(); // WTQRCodeDesignUpdateParams | 

            try
            {
                // Update QR Code Design
                WTQRCodeDesign result = apiInstance.UpdateQRCodeDesign(id, wTQRCodeDesignUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QRCodeDesignsApi.UpdateQRCodeDesign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateQRCodeDesignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update QR Code Design
    ApiResponse<WTQRCodeDesign> response = apiInstance.UpdateQRCodeDesignWithHttpInfo(id, wTQRCodeDesignUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QRCodeDesignsApi.UpdateQRCodeDesignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTQRCodeDesignUpdateParams** | [**WTQRCodeDesignUpdateParams**](WTQRCodeDesignUpdateParams.md) |  |  |

### Return type

[**WTQRCodeDesign**](WTQRCodeDesign.md)

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

