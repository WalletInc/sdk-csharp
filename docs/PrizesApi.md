# WalletInc.Api.PrizesApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveAdvertisementCredit**](PrizesApi.md#archiveadvertisementcredit) | **DELETE** /v2/payment/advertisementCredit/{id} | Archive Prize |
| [**CreateAdvertisementCredit**](PrizesApi.md#createadvertisementcredit) | **POST** /v2/payment/advertisementCredit | Create Prize |
| [**FetchAdvertisementCreditById**](PrizesApi.md#fetchadvertisementcreditbyid) | **GET** /v2/payment/advertisementCredit/{id} | Get Prize |
| [**FetchAdvertisementCreditScans**](PrizesApi.md#fetchadvertisementcreditscans) | **GET** /v2/payment/advertisementCredit/scans/{id} | Get Prizes awarded |
| [**FetchAllAdvertisementCredits**](PrizesApi.md#fetchalladvertisementcredits) | **GET** /v2/payment/advertisementCredit/all | Get all Prizes |
| [**RestoreAdvertisementCredit**](PrizesApi.md#restoreadvertisementcredit) | **PATCH** /v2/payment/advertisementCredit/{id} | Restore Prize |
| [**UpdateAdvertisementCredit**](PrizesApi.md#updateadvertisementcredit) | **PUT** /v2/payment/advertisementCredit/{id} | Update Prize |

<a id="archiveadvertisementcredit"></a>
# **ArchiveAdvertisementCredit**
> WTAdvertisementCredit ArchiveAdvertisementCredit (string id)

Archive Prize

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
    public class ArchiveAdvertisementCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new PrizesApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive Prize
                WTAdvertisementCredit result = apiInstance.ArchiveAdvertisementCredit(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PrizesApi.ArchiveAdvertisementCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveAdvertisementCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Prize
    ApiResponse<WTAdvertisementCredit> response = apiInstance.ArchiveAdvertisementCreditWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PrizesApi.ArchiveAdvertisementCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTAdvertisementCredit**](WTAdvertisementCredit.md)

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

<a id="createadvertisementcredit"></a>
# **CreateAdvertisementCredit**
> WTAdvertisementCredit CreateAdvertisementCredit (WTAdvertisementCreditCreateParams wTAdvertisementCreditCreateParams)

Create Prize

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
    public class CreateAdvertisementCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new PrizesApi(httpClient, config, httpClientHandler);
            var wTAdvertisementCreditCreateParams = new WTAdvertisementCreditCreateParams(); // WTAdvertisementCreditCreateParams | 

            try
            {
                // Create Prize
                WTAdvertisementCredit result = apiInstance.CreateAdvertisementCredit(wTAdvertisementCreditCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PrizesApi.CreateAdvertisementCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdvertisementCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Prize
    ApiResponse<WTAdvertisementCredit> response = apiInstance.CreateAdvertisementCreditWithHttpInfo(wTAdvertisementCreditCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PrizesApi.CreateAdvertisementCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTAdvertisementCreditCreateParams** | [**WTAdvertisementCreditCreateParams**](WTAdvertisementCreditCreateParams.md) |  |  |

### Return type

[**WTAdvertisementCredit**](WTAdvertisementCredit.md)

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

<a id="fetchadvertisementcreditbyid"></a>
# **FetchAdvertisementCreditById**
> WTAdvertisementCredit FetchAdvertisementCreditById (string id)

Get Prize

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
    public class FetchAdvertisementCreditByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new PrizesApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Prize
                WTAdvertisementCredit result = apiInstance.FetchAdvertisementCreditById(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PrizesApi.FetchAdvertisementCreditById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAdvertisementCreditByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Prize
    ApiResponse<WTAdvertisementCredit> response = apiInstance.FetchAdvertisementCreditByIdWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PrizesApi.FetchAdvertisementCreditByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTAdvertisementCredit**](WTAdvertisementCredit.md)

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

<a id="fetchadvertisementcreditscans"></a>
# **FetchAdvertisementCreditScans**
> List&lt;WTAdvertisementCreditScan&gt; FetchAdvertisementCreditScans (string id)

Get Prizes awarded

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
    public class FetchAdvertisementCreditScansExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new PrizesApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Prizes awarded
                List<WTAdvertisementCreditScan> result = apiInstance.FetchAdvertisementCreditScans(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PrizesApi.FetchAdvertisementCreditScans: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAdvertisementCreditScansWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Prizes awarded
    ApiResponse<List<WTAdvertisementCreditScan>> response = apiInstance.FetchAdvertisementCreditScansWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PrizesApi.FetchAdvertisementCreditScansWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**List&lt;WTAdvertisementCreditScan&gt;**](WTAdvertisementCreditScan.md)

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

<a id="fetchalladvertisementcredits"></a>
# **FetchAllAdvertisementCredits**
> List&lt;WTAdvertisementCredit&gt; FetchAllAdvertisementCredits (bool? isArchiveIncluded = null)

Get all Prizes

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
    public class FetchAllAdvertisementCreditsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new PrizesApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all Prizes
                List<WTAdvertisementCredit> result = apiInstance.FetchAllAdvertisementCredits(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PrizesApi.FetchAllAdvertisementCredits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllAdvertisementCreditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Prizes
    ApiResponse<List<WTAdvertisementCredit>> response = apiInstance.FetchAllAdvertisementCreditsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PrizesApi.FetchAllAdvertisementCreditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;WTAdvertisementCredit&gt;**](WTAdvertisementCredit.md)

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

<a id="restoreadvertisementcredit"></a>
# **RestoreAdvertisementCredit**
> WTAdvertisementCredit RestoreAdvertisementCredit (string id)

Restore Prize

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
    public class RestoreAdvertisementCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new PrizesApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore Prize
                WTAdvertisementCredit result = apiInstance.RestoreAdvertisementCredit(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PrizesApi.RestoreAdvertisementCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreAdvertisementCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Prize
    ApiResponse<WTAdvertisementCredit> response = apiInstance.RestoreAdvertisementCreditWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PrizesApi.RestoreAdvertisementCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTAdvertisementCredit**](WTAdvertisementCredit.md)

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

<a id="updateadvertisementcredit"></a>
# **UpdateAdvertisementCredit**
> WTAdvertisementCredit UpdateAdvertisementCredit (string id, WTAdvertisementCreditUpdateParams wTAdvertisementCreditUpdateParams)

Update Prize

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
    public class UpdateAdvertisementCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new PrizesApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTAdvertisementCreditUpdateParams = new WTAdvertisementCreditUpdateParams(); // WTAdvertisementCreditUpdateParams | 

            try
            {
                // Update Prize
                WTAdvertisementCredit result = apiInstance.UpdateAdvertisementCredit(id, wTAdvertisementCreditUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PrizesApi.UpdateAdvertisementCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAdvertisementCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Prize
    ApiResponse<WTAdvertisementCredit> response = apiInstance.UpdateAdvertisementCreditWithHttpInfo(id, wTAdvertisementCreditUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PrizesApi.UpdateAdvertisementCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTAdvertisementCreditUpdateParams** | [**WTAdvertisementCreditUpdateParams**](WTAdvertisementCreditUpdateParams.md) |  |  |

### Return type

[**WTAdvertisementCredit**](WTAdvertisementCredit.md)

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

