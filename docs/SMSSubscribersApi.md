# WalletInc.Api.SMSSubscribersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveSmsSubscriber**](SMSSubscribersApi.md#archivesmssubscriber) | **DELETE** /v2/SmsSubscriber/{id} | Archive SMS Subscriber |
| [**CreateSmsSubscriber**](SMSSubscribersApi.md#createsmssubscriber) | **POST** /v2/SmsSubscriber | Create SMS Subscriber |
| [**FetchAllSmsSubscribers**](SMSSubscribersApi.md#fetchallsmssubscribers) | **GET** /v2/SmsSubscriber/all | Get all SMS Subscribers |
| [**RestoreSmsSubscriber**](SMSSubscribersApi.md#restoresmssubscriber) | **PATCH** /v2/SmsSubscriber/{id} | Restore SMS Subscriber |
| [**UpdateSmsSubscriber**](SMSSubscribersApi.md#updatesmssubscriber) | **PUT** /v2/SmsSubscriber/{id} | Update SMS Subscriber |

<a id="archivesmssubscriber"></a>
# **ArchiveSmsSubscriber**
> SmsSubscriber ArchiveSmsSubscriber (string id)

Archive SMS Subscriber

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
    public class ArchiveSmsSubscriberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive SMS Subscriber
                SmsSubscriber result = apiInstance.ArchiveSmsSubscriber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.ArchiveSmsSubscriber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveSmsSubscriberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive SMS Subscriber
    ApiResponse<SmsSubscriber> response = apiInstance.ArchiveSmsSubscriberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.ArchiveSmsSubscriberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**SmsSubscriber**](SmsSubscriber.md)

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

<a id="createsmssubscriber"></a>
# **CreateSmsSubscriber**
> SmsSubscriber CreateSmsSubscriber (WTSmsSubscriberCreateParams wTSmsSubscriberCreateParams)

Create SMS Subscriber

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
    public class CreateSmsSubscriberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);
            var wTSmsSubscriberCreateParams = new WTSmsSubscriberCreateParams(); // WTSmsSubscriberCreateParams | 

            try
            {
                // Create SMS Subscriber
                SmsSubscriber result = apiInstance.CreateSmsSubscriber(wTSmsSubscriberCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.CreateSmsSubscriber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSmsSubscriberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create SMS Subscriber
    ApiResponse<SmsSubscriber> response = apiInstance.CreateSmsSubscriberWithHttpInfo(wTSmsSubscriberCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.CreateSmsSubscriberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTSmsSubscriberCreateParams** | [**WTSmsSubscriberCreateParams**](WTSmsSubscriberCreateParams.md) |  |  |

### Return type

[**SmsSubscriber**](SmsSubscriber.md)

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

<a id="fetchallsmssubscribers"></a>
# **FetchAllSmsSubscribers**
> Object FetchAllSmsSubscribers (DateTime? startDateTime = null, DateTime? endDateTime = null, bool? isArchiveIncluded = null)

Get all SMS Subscribers

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
    public class FetchAllSmsSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all SMS Subscribers
                Object result = apiInstance.FetchAllSmsSubscribers(startDateTime, endDateTime, isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.FetchAllSmsSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllSmsSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all SMS Subscribers
    ApiResponse<Object> response = apiInstance.FetchAllSmsSubscribersWithHttpInfo(startDateTime, endDateTime, isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.FetchAllSmsSubscribersWithHttpInfo: " + e.Message);
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

<a id="restoresmssubscriber"></a>
# **RestoreSmsSubscriber**
> SmsSubscriber RestoreSmsSubscriber (string id)

Restore SMS Subscriber

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
    public class RestoreSmsSubscriberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore SMS Subscriber
                SmsSubscriber result = apiInstance.RestoreSmsSubscriber(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.RestoreSmsSubscriber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreSmsSubscriberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore SMS Subscriber
    ApiResponse<SmsSubscriber> response = apiInstance.RestoreSmsSubscriberWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.RestoreSmsSubscriberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**SmsSubscriber**](SmsSubscriber.md)

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

<a id="updatesmssubscriber"></a>
# **UpdateSmsSubscriber**
> SmsSubscriber UpdateSmsSubscriber (string id, WTSmsSubscriberUpdateParams wTSmsSubscriberUpdateParams)

Update SMS Subscriber

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
    public class UpdateSmsSubscriberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var wTSmsSubscriberUpdateParams = new WTSmsSubscriberUpdateParams(); // WTSmsSubscriberUpdateParams | 

            try
            {
                // Update SMS Subscriber
                SmsSubscriber result = apiInstance.UpdateSmsSubscriber(id, wTSmsSubscriberUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.UpdateSmsSubscriber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSmsSubscriberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update SMS Subscriber
    ApiResponse<SmsSubscriber> response = apiInstance.UpdateSmsSubscriberWithHttpInfo(id, wTSmsSubscriberUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.UpdateSmsSubscriberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **wTSmsSubscriberUpdateParams** | [**WTSmsSubscriberUpdateParams**](WTSmsSubscriberUpdateParams.md) |  |  |

### Return type

[**SmsSubscriber**](SmsSubscriber.md)

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

