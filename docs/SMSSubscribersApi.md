# WalletInc.Api.SMSSubscribersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveSmsSubscriber**](SMSSubscribersApi.md#archivesmssubscriber) | **DELETE** /v2/SmsSubscriber/{id} | Archive SMS Subscriber |
| [**CountEarlySmsOptIns**](SMSSubscribersApi.md#countearlysmsoptins) | **GET** /sms/earlyOptIns/count | Count early SMS opt-ins |
| [**CreateSmsSubscriber**](SMSSubscribersApi.md#createsmssubscriber) | **POST** /v2/SmsSubscriber | Create SMS Subscriber |
| [**FetchAllSmsSubscribers**](SMSSubscribersApi.md#fetchallsmssubscribers) | **GET** /v2/SmsSubscriber/all | Get all SMS Subscribers |
| [**FetchEarlySmsOptIns**](SMSSubscribersApi.md#fetchearlysmsoptins) | **GET** /sms/earlyOptIns | List early SMS opt-ins |
| [**ImportEarlySmsOptIns**](SMSSubscribersApi.md#importearlysmsoptins) | **POST** /sms/earlyOptIns/import | Bring early SMS opt-ins over |
| [**PreviewEarlySmsOptInImport**](SMSSubscribersApi.md#previewearlysmsoptinimport) | **GET** /sms/earlyOptIns/importPreview | Preview bringing early SMS opt-ins over |
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

<a id="countearlysmsoptins"></a>
# **CountEarlySmsOptIns**
> WTEarlyOptInCount CountEarlySmsOptIns ()

Count early SMS opt-ins

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
    public class CountEarlySmsOptInsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);

            try
            {
                // Count early SMS opt-ins
                WTEarlyOptInCount result = apiInstance.CountEarlySmsOptIns();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.CountEarlySmsOptIns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountEarlySmsOptInsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count early SMS opt-ins
    ApiResponse<WTEarlyOptInCount> response = apiInstance.CountEarlySmsOptInsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.CountEarlySmsOptInsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**WTEarlyOptInCount**](WTEarlyOptInCount.md)

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

<a id="fetchearlysmsoptins"></a>
# **FetchEarlySmsOptIns**
> WTEarlyOptInPage FetchEarlySmsOptIns (double? page = null, double? pageSize = null)

List early SMS opt-ins

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
    public class FetchEarlySmsOptInsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);
            var page = 1.2D;  // double? |  (optional) 
            var pageSize = 1.2D;  // double? |  (optional) 

            try
            {
                // List early SMS opt-ins
                WTEarlyOptInPage result = apiInstance.FetchEarlySmsOptIns(page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.FetchEarlySmsOptIns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchEarlySmsOptInsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List early SMS opt-ins
    ApiResponse<WTEarlyOptInPage> response = apiInstance.FetchEarlySmsOptInsWithHttpInfo(page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.FetchEarlySmsOptInsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **double?** |  | [optional]  |
| **pageSize** | **double?** |  | [optional]  |

### Return type

[**WTEarlyOptInPage**](WTEarlyOptInPage.md)

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
| **403** | Upgrade required to see the list |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="importearlysmsoptins"></a>
# **ImportEarlySmsOptIns**
> WTEarlyOptInImportResult ImportEarlySmsOptIns (WTEarlyOptInImportRequest? wTEarlyOptInImportRequest = null)

Bring early SMS opt-ins over

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
    public class ImportEarlySmsOptInsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);
            var wTEarlyOptInImportRequest = new WTEarlyOptInImportRequest?(); // WTEarlyOptInImportRequest? |  (optional) 

            try
            {
                // Bring early SMS opt-ins over
                WTEarlyOptInImportResult result = apiInstance.ImportEarlySmsOptIns(wTEarlyOptInImportRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.ImportEarlySmsOptIns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImportEarlySmsOptInsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Bring early SMS opt-ins over
    ApiResponse<WTEarlyOptInImportResult> response = apiInstance.ImportEarlySmsOptInsWithHttpInfo(wTEarlyOptInImportRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.ImportEarlySmsOptInsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEarlyOptInImportRequest** | [**WTEarlyOptInImportRequest?**](WTEarlyOptInImportRequest?.md) |  | [optional]  |

### Return type

[**WTEarlyOptInImportResult**](WTEarlyOptInImportResult.md)

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
| **413** | Entity Too Large |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="previewearlysmsoptinimport"></a>
# **PreviewEarlySmsOptInImport**
> WTEarlyOptInImportResult PreviewEarlySmsOptInImport ()

Preview bringing early SMS opt-ins over

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
    public class PreviewEarlySmsOptInImportExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSSubscribersApi(httpClient, config, httpClientHandler);

            try
            {
                // Preview bringing early SMS opt-ins over
                WTEarlyOptInImportResult result = apiInstance.PreviewEarlySmsOptInImport();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSSubscribersApi.PreviewEarlySmsOptInImport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewEarlySmsOptInImportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview bringing early SMS opt-ins over
    ApiResponse<WTEarlyOptInImportResult> response = apiInstance.PreviewEarlySmsOptInImportWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSSubscribersApi.PreviewEarlySmsOptInImportWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**WTEarlyOptInImportResult**](WTEarlyOptInImportResult.md)

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

