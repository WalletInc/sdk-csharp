# WalletInc.Api.APIKeysApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveEmployeeAPIKeys**](APIKeysApi.md#archiveemployeeapikeys) | **DELETE** /v2/employee/apiKeys/{id} | Archive API Key |
| [**CreateEmployeeAPIKeys**](APIKeysApi.md#createemployeeapikeys) | **POST** /v2/employee/apiKeys | Create API Key |
| [**FetchAllEmployeeAPIKeys**](APIKeysApi.md#fetchallemployeeapikeys) | **GET** /v2/employee/apiKeys/all | Get API Keys |
| [**FetchEmployeeAPIKeyById**](APIKeysApi.md#fetchemployeeapikeybyid) | **GET** /v2/employee/apiKeys/{id} | Get API Key |
| [**UpdateEmployeeAPIKeys**](APIKeysApi.md#updateemployeeapikeys) | **PUT** /v2/employee/apiKeys/{id} | Update API Key |

<a id="archiveemployeeapikeys"></a>
# **ArchiveEmployeeAPIKeys**
> EmployeeAPIKey ArchiveEmployeeAPIKeys (string id)

Archive API Key

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
    public class ArchiveEmployeeAPIKeysExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new APIKeysApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive API Key
                EmployeeAPIKey result = apiInstance.ArchiveEmployeeAPIKeys(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIKeysApi.ArchiveEmployeeAPIKeys: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveEmployeeAPIKeysWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive API Key
    ApiResponse<EmployeeAPIKey> response = apiInstance.ArchiveEmployeeAPIKeysWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIKeysApi.ArchiveEmployeeAPIKeysWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**EmployeeAPIKey**](EmployeeAPIKey.md)

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

<a id="createemployeeapikeys"></a>
# **CreateEmployeeAPIKeys**
> EmployeeAPIKey CreateEmployeeAPIKeys (WTEmployeeAPIKeyCreateParams wTEmployeeAPIKeyCreateParams)

Create API Key

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
    public class CreateEmployeeAPIKeysExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new APIKeysApi(httpClient, config, httpClientHandler);
            var wTEmployeeAPIKeyCreateParams = new WTEmployeeAPIKeyCreateParams(); // WTEmployeeAPIKeyCreateParams | 

            try
            {
                // Create API Key
                EmployeeAPIKey result = apiInstance.CreateEmployeeAPIKeys(wTEmployeeAPIKeyCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIKeysApi.CreateEmployeeAPIKeys: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEmployeeAPIKeysWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create API Key
    ApiResponse<EmployeeAPIKey> response = apiInstance.CreateEmployeeAPIKeysWithHttpInfo(wTEmployeeAPIKeyCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIKeysApi.CreateEmployeeAPIKeysWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeAPIKeyCreateParams** | [**WTEmployeeAPIKeyCreateParams**](WTEmployeeAPIKeyCreateParams.md) |  |  |

### Return type

[**EmployeeAPIKey**](EmployeeAPIKey.md)

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

<a id="fetchallemployeeapikeys"></a>
# **FetchAllEmployeeAPIKeys**
> List&lt;EmployeeAPIKey&gt; FetchAllEmployeeAPIKeys (bool? isArchiveIncluded = null)

Get API Keys

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
    public class FetchAllEmployeeAPIKeysExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new APIKeysApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get API Keys
                List<EmployeeAPIKey> result = apiInstance.FetchAllEmployeeAPIKeys(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIKeysApi.FetchAllEmployeeAPIKeys: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllEmployeeAPIKeysWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get API Keys
    ApiResponse<List<EmployeeAPIKey>> response = apiInstance.FetchAllEmployeeAPIKeysWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIKeysApi.FetchAllEmployeeAPIKeysWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;EmployeeAPIKey&gt;**](EmployeeAPIKey.md)

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

<a id="fetchemployeeapikeybyid"></a>
# **FetchEmployeeAPIKeyById**
> WTEmployeeAPIKey FetchEmployeeAPIKeyById (string id)

Get API Key

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
    public class FetchEmployeeAPIKeyByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new APIKeysApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get API Key
                WTEmployeeAPIKey result = apiInstance.FetchEmployeeAPIKeyById(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIKeysApi.FetchEmployeeAPIKeyById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchEmployeeAPIKeyByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get API Key
    ApiResponse<WTEmployeeAPIKey> response = apiInstance.FetchEmployeeAPIKeyByIdWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIKeysApi.FetchEmployeeAPIKeyByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**WTEmployeeAPIKey**](WTEmployeeAPIKey.md)

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

<a id="updateemployeeapikeys"></a>
# **UpdateEmployeeAPIKeys**
> EmployeeAPIKey UpdateEmployeeAPIKeys (string id, WTEmployeeAPIKeyUpdateParams wTEmployeeAPIKeyUpdateParams)

Update API Key

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
    public class UpdateEmployeeAPIKeysExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new APIKeysApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTEmployeeAPIKeyUpdateParams = new WTEmployeeAPIKeyUpdateParams(); // WTEmployeeAPIKeyUpdateParams | 

            try
            {
                // Update API Key
                EmployeeAPIKey result = apiInstance.UpdateEmployeeAPIKeys(id, wTEmployeeAPIKeyUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIKeysApi.UpdateEmployeeAPIKeys: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEmployeeAPIKeysWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update API Key
    ApiResponse<EmployeeAPIKey> response = apiInstance.UpdateEmployeeAPIKeysWithHttpInfo(id, wTEmployeeAPIKeyUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIKeysApi.UpdateEmployeeAPIKeysWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTEmployeeAPIKeyUpdateParams** | [**WTEmployeeAPIKeyUpdateParams**](WTEmployeeAPIKeyUpdateParams.md) |  |  |

### Return type

[**EmployeeAPIKey**](EmployeeAPIKey.md)

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

