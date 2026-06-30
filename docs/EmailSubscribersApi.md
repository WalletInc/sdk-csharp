# WalletInc.Api.EmailSubscribersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveEmailSubscriber**](EmailSubscribersApi.md#archiveemailsubscriber) | **DELETE** /v2/emailSubscriber/{id} | Archive Email Subscriber |
| [**CreateEmailSubscriber**](EmailSubscribersApi.md#createemailsubscriber) | **POST** /v2/emailSubscriber | Create Email Subscriber |
| [**FetchAllEmailSubscribers**](EmailSubscribersApi.md#fetchallemailsubscribers) | **GET** /v2/emailSubscriber/all | Get all Email Subscribers |
| [**RestoreEmailSubscriber**](EmailSubscribersApi.md#restoreemailsubscriber) | **PATCH** /v2/emailSubscriber/{id} | Restore Email Subscriber |
| [**UpdateEmailSubscriber**](EmailSubscribersApi.md#updateemailsubscriber) | **PUT** /v2/emailSubscriber/{id} | Update Email Subscriber |

<a id="archiveemailsubscriber"></a>
# **ArchiveEmailSubscriber**
> EmailSubscriber ArchiveEmailSubscriber (string id)

Archive Email Subscriber

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
    public class ArchiveEmailSubscriberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmailSubscribersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive Email Subscriber
                EmailSubscriber result = apiInstance.ArchiveEmailSubscriber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailSubscribersApi.ArchiveEmailSubscriber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveEmailSubscriberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Email Subscriber
    ApiResponse<EmailSubscriber> response = apiInstance.ArchiveEmailSubscriberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailSubscribersApi.ArchiveEmailSubscriberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**EmailSubscriber**](EmailSubscriber.md)

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

<a id="createemailsubscriber"></a>
# **CreateEmailSubscriber**
> EmailSubscriber CreateEmailSubscriber (WTEmailSubscriberCreateParams wTEmailSubscriberCreateParams)

Create Email Subscriber

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
    public class CreateEmailSubscriberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmailSubscribersApi(httpClient, config, httpClientHandler);
            var wTEmailSubscriberCreateParams = new WTEmailSubscriberCreateParams(); // WTEmailSubscriberCreateParams | 

            try
            {
                // Create Email Subscriber
                EmailSubscriber result = apiInstance.CreateEmailSubscriber(wTEmailSubscriberCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailSubscribersApi.CreateEmailSubscriber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEmailSubscriberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Email Subscriber
    ApiResponse<EmailSubscriber> response = apiInstance.CreateEmailSubscriberWithHttpInfo(wTEmailSubscriberCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailSubscribersApi.CreateEmailSubscriberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmailSubscriberCreateParams** | [**WTEmailSubscriberCreateParams**](WTEmailSubscriberCreateParams.md) |  |  |

### Return type

[**EmailSubscriber**](EmailSubscriber.md)

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

<a id="fetchallemailsubscribers"></a>
# **FetchAllEmailSubscribers**
> Object FetchAllEmailSubscribers (DateTime? startDateTime = null, DateTime? endDateTime = null, bool? isArchiveIncluded = null)

Get all Email Subscribers

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
    public class FetchAllEmailSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmailSubscribersApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all Email Subscribers
                Object result = apiInstance.FetchAllEmailSubscribers(startDateTime, endDateTime, isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailSubscribersApi.FetchAllEmailSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllEmailSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Email Subscribers
    ApiResponse<Object> response = apiInstance.FetchAllEmailSubscribersWithHttpInfo(startDateTime, endDateTime, isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailSubscribersApi.FetchAllEmailSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime?** |  | [optional]  |
| **endDateTime** | **DateTime?** |  | [optional]  |
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

<a id="restoreemailsubscriber"></a>
# **RestoreEmailSubscriber**
> EmailSubscriber RestoreEmailSubscriber (string id)

Restore Email Subscriber

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
    public class RestoreEmailSubscriberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmailSubscribersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore Email Subscriber
                EmailSubscriber result = apiInstance.RestoreEmailSubscriber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailSubscribersApi.RestoreEmailSubscriber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreEmailSubscriberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Email Subscriber
    ApiResponse<EmailSubscriber> response = apiInstance.RestoreEmailSubscriberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailSubscribersApi.RestoreEmailSubscriberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**EmailSubscriber**](EmailSubscriber.md)

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

<a id="updateemailsubscriber"></a>
# **UpdateEmailSubscriber**
> EmailSubscriber UpdateEmailSubscriber (string id, WTEmailSubscriberUpdateParams wTEmailSubscriberUpdateParams)

Update Email Subscriber

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
    public class UpdateEmailSubscriberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmailSubscribersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTEmailSubscriberUpdateParams = new WTEmailSubscriberUpdateParams(); // WTEmailSubscriberUpdateParams | 

            try
            {
                // Update Email Subscriber
                EmailSubscriber result = apiInstance.UpdateEmailSubscriber(id, wTEmailSubscriberUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmailSubscribersApi.UpdateEmailSubscriber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEmailSubscriberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Email Subscriber
    ApiResponse<EmailSubscriber> response = apiInstance.UpdateEmailSubscriberWithHttpInfo(id, wTEmailSubscriberUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmailSubscribersApi.UpdateEmailSubscriberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTEmailSubscriberUpdateParams** | [**WTEmailSubscriberUpdateParams**](WTEmailSubscriberUpdateParams.md) |  |  |

### Return type

[**EmailSubscriber**](EmailSubscriber.md)

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

