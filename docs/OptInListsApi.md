# WalletInc.Api.OptInListsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CountOptInListSubscribers**](OptInListsApi.md#countoptinlistsubscribers) | **GET** /v2/sms/optInList/subscribers/count/{listID} | Count opt in list subscribers |
| [**CountOptInSourceSubscribers**](OptInListsApi.md#countoptinsourcesubscribers) | **GET** /v2/sms/optInSource/subscribers/count/{sourceID} | Count opt in source subscribers |
| [**CreateOptInList**](OptInListsApi.md#createoptinlist) | **POST** /v2/sms/optInList | Create opt in list |
| [**CreateOptInListSource**](OptInListsApi.md#createoptinlistsource) | **POST** /v2/sms/optInListSource | Send SMS to opt in list |
| [**ExportOptInListSubscribers**](OptInListsApi.md#exportoptinlistsubscribers) | **POST** /v2/sms/optInList/subscribers/export/{listID} | Export opt in list subscribers |
| [**FetchOptInList**](OptInListsApi.md#fetchoptinlist) | **GET** /v2/merchant/lists/optIn/{listID} | Get opt in list |
| [**FetchOptInListSource**](OptInListsApi.md#fetchoptinlistsource) | **GET** /v2/employee/optInListSource/{sourceID} | Get opt in list source |
| [**FetchOptInListSources**](OptInListsApi.md#fetchoptinlistsources) | **GET** /v2/sms/optInListSources/all | Get all opt in list sources |
| [**FetchOptInListSourcesCreatedByEmployee**](OptInListsApi.md#fetchoptinlistsourcescreatedbyemployee) | **GET** /v2/employee/optInListSources/all | Get all opt in list sources |
| [**FetchOptInListSubscribers**](OptInListsApi.md#fetchoptinlistsubscribers) | **GET** /v2/sms/optInList/subscribers/{listID} | Get opt in list subscribers |
| [**FetchOptInListSubscribersByPage**](OptInListsApi.md#fetchoptinlistsubscribersbypage) | **GET** /v2/sms/optInList/subscribers/page/{listID} | Get opt in list subscribers by page |
| [**FetchOptInLists**](OptInListsApi.md#fetchoptinlists) | **GET** /v2/merchant/lists/optIn/all | Get all opt in lists |
| [**FetchOptInListsAssociatedWithPhoneNumber**](OptInListsApi.md#fetchoptinlistsassociatedwithphonenumber) | **GET** /v2/sms/phoneNumber/lists/{phoneNumberID} | Get opt in lists |
| [**FetchOptInSourceSubscribers**](OptInListsApi.md#fetchoptinsourcesubscribers) | **GET** /v2/sms/optInSource/subscribers/{sourceID} | Get opt in source subscribers |
| [**FetchOptInSourcesAssociatedWithPhoneNumber**](OptInListsApi.md#fetchoptinsourcesassociatedwithphonenumber) | **GET** /v2/sms/phoneNumber/sources/{phoneNumberID} | Get opt in sources |
| [**ImportOptInListSubscribers**](OptInListsApi.md#importoptinlistsubscribers) | **POST** /v2/sms/optInList/subscribers/import/{listID} | Import opt in list subscribers |
| [**SaveOptInList**](OptInListsApi.md#saveoptinlist) | **PUT** /v2/sms/optInList/{listID} | Save opt in list |
| [**SaveOptInListSource**](OptInListsApi.md#saveoptinlistsource) | **PUT** /v2/sms/optInListSource/{sourceID} | Save opt in list source |

<a id="countoptinlistsubscribers"></a>
# **CountOptInListSubscribers**
> WTCountResult CountOptInListSubscribers (string listID, bool? isSubscribed = null, bool? isPendingAge21Verification = null, bool? isArchiveIncluded = null, DateTime? startDate = null, DateTime? endDate = null)

Count opt in list subscribers

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
    public class CountOptInListSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var isSubscribed = true;  // bool? |  (optional) 
            var isPendingAge21Verification = true;  // bool? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count opt in list subscribers
                WTCountResult result = apiInstance.CountOptInListSubscribers(listID, isSubscribed, isPendingAge21Verification, isArchiveIncluded, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.CountOptInListSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountOptInListSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count opt in list subscribers
    ApiResponse<WTCountResult> response = apiInstance.CountOptInListSubscribersWithHttpInfo(listID, isSubscribed, isPendingAge21Verification, isArchiveIncluded, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.CountOptInListSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **isSubscribed** | **bool?** |  | [optional]  |
| **isPendingAge21Verification** | **bool?** |  | [optional]  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countoptinsourcesubscribers"></a>
# **CountOptInSourceSubscribers**
> WTCountResult CountOptInSourceSubscribers (string sourceID, bool? isSubscribed = null, bool? isPendingAge21Verification = null, bool? isArchiveIncluded = null, DateTime? startDate = null, DateTime? endDate = null)

Count opt in source subscribers

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
    public class CountOptInSourceSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var sourceID = "sourceID_example";  // string | 
            var isSubscribed = true;  // bool? |  (optional) 
            var isPendingAge21Verification = true;  // bool? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count opt in source subscribers
                WTCountResult result = apiInstance.CountOptInSourceSubscribers(sourceID, isSubscribed, isPendingAge21Verification, isArchiveIncluded, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.CountOptInSourceSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountOptInSourceSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count opt in source subscribers
    ApiResponse<WTCountResult> response = apiInstance.CountOptInSourceSubscribersWithHttpInfo(sourceID, isSubscribed, isPendingAge21Verification, isArchiveIncluded, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.CountOptInSourceSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sourceID** | **string** |  |  |
| **isSubscribed** | **bool?** |  | [optional]  |
| **isPendingAge21Verification** | **bool?** |  | [optional]  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="createoptinlist"></a>
# **CreateOptInList**
> OptInList CreateOptInList (WTOptInListCreationParams wTOptInListCreationParams)

Create opt in list

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
    public class CreateOptInListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var wTOptInListCreationParams = new WTOptInListCreationParams(); // WTOptInListCreationParams | 

            try
            {
                // Create opt in list
                OptInList result = apiInstance.CreateOptInList(wTOptInListCreationParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.CreateOptInList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateOptInListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create opt in list
    ApiResponse<OptInList> response = apiInstance.CreateOptInListWithHttpInfo(wTOptInListCreationParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.CreateOptInListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTOptInListCreationParams** | [**WTOptInListCreationParams**](WTOptInListCreationParams.md) |  |  |

### Return type

[**OptInList**](OptInList.md)

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

<a id="createoptinlistsource"></a>
# **CreateOptInListSource**
> OptInListSource CreateOptInListSource (WTSMSOptInListSourceCreate wTSMSOptInListSourceCreate)

Send SMS to opt in list

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
    public class CreateOptInListSourceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var wTSMSOptInListSourceCreate = new WTSMSOptInListSourceCreate(); // WTSMSOptInListSourceCreate | 

            try
            {
                // Send SMS to opt in list
                OptInListSource result = apiInstance.CreateOptInListSource(wTSMSOptInListSourceCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.CreateOptInListSource: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateOptInListSourceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send SMS to opt in list
    ApiResponse<OptInListSource> response = apiInstance.CreateOptInListSourceWithHttpInfo(wTSMSOptInListSourceCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.CreateOptInListSourceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTSMSOptInListSourceCreate** | [**WTSMSOptInListSourceCreate**](WTSMSOptInListSourceCreate.md) |  |  |

### Return type

[**OptInListSource**](OptInListSource.md)

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

<a id="exportoptinlistsubscribers"></a>
# **ExportOptInListSubscribers**
> string ExportOptInListSubscribers (string listID)

Export opt in list subscribers

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
    public class ExportOptInListSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 

            try
            {
                // Export opt in list subscribers
                string result = apiInstance.ExportOptInListSubscribers(listID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.ExportOptInListSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportOptInListSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export opt in list subscribers
    ApiResponse<string> response = apiInstance.ExportOptInListSubscribersWithHttpInfo(listID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.ExportOptInListSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |

### Return type

**string**

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

<a id="fetchoptinlist"></a>
# **FetchOptInList**
> OptInList FetchOptInList (string listID)

Get opt in list

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
    public class FetchOptInListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 

            try
            {
                // Get opt in list
                OptInList result = apiInstance.FetchOptInList(listID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get opt in list
    ApiResponse<OptInList> response = apiInstance.FetchOptInListWithHttpInfo(listID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |

### Return type

[**OptInList**](OptInList.md)

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

<a id="fetchoptinlistsource"></a>
# **FetchOptInListSource**
> OptInListSource FetchOptInListSource (string sourceID)

Get opt in list source

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
    public class FetchOptInListSourceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var sourceID = "sourceID_example";  // string | 

            try
            {
                // Get opt in list source
                OptInListSource result = apiInstance.FetchOptInListSource(sourceID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInListSource: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListSourceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get opt in list source
    ApiResponse<OptInListSource> response = apiInstance.FetchOptInListSourceWithHttpInfo(sourceID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInListSourceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sourceID** | **string** |  |  |

### Return type

[**OptInListSource**](OptInListSource.md)

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

<a id="fetchoptinlistsources"></a>
# **FetchOptInListSources**
> Object FetchOptInListSources (bool? isArchiveIncluded = null)

Get all opt in list sources

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
    public class FetchOptInListSourcesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all opt in list sources
                Object result = apiInstance.FetchOptInListSources(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInListSources: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListSourcesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all opt in list sources
    ApiResponse<Object> response = apiInstance.FetchOptInListSourcesWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInListSourcesWithHttpInfo: " + e.Message);
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

<a id="fetchoptinlistsourcescreatedbyemployee"></a>
# **FetchOptInListSourcesCreatedByEmployee**
> List&lt;OptInListSource&gt; FetchOptInListSourcesCreatedByEmployee ()

Get all opt in list sources

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
    public class FetchOptInListSourcesCreatedByEmployeeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);

            try
            {
                // Get all opt in list sources
                List<OptInListSource> result = apiInstance.FetchOptInListSourcesCreatedByEmployee();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInListSourcesCreatedByEmployee: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListSourcesCreatedByEmployeeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all opt in list sources
    ApiResponse<List<OptInListSource>> response = apiInstance.FetchOptInListSourcesCreatedByEmployeeWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInListSourcesCreatedByEmployeeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;OptInListSource&gt;**](OptInListSource.md)

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

<a id="fetchoptinlistsubscribers"></a>
# **FetchOptInListSubscribers**
> List&lt;OptInListSubscriber&gt; FetchOptInListSubscribers (string listID, bool? isSubscribed = null, bool? isPendingAge21Verification = null, bool? isArchiveIncluded = null)

Get opt in list subscribers

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
    public class FetchOptInListSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var isSubscribed = true;  // bool? |  (optional) 
            var isPendingAge21Verification = true;  // bool? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get opt in list subscribers
                List<OptInListSubscriber> result = apiInstance.FetchOptInListSubscribers(listID, isSubscribed, isPendingAge21Verification, isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInListSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get opt in list subscribers
    ApiResponse<List<OptInListSubscriber>> response = apiInstance.FetchOptInListSubscribersWithHttpInfo(listID, isSubscribed, isPendingAge21Verification, isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInListSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **isSubscribed** | **bool?** |  | [optional]  |
| **isPendingAge21Verification** | **bool?** |  | [optional]  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;OptInListSubscriber&gt;**](OptInListSubscriber.md)

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

<a id="fetchoptinlistsubscribersbypage"></a>
# **FetchOptInListSubscribersByPage**
> FetchOptInListSubscribersByPage200Response FetchOptInListSubscribersByPage (string listID, double? pageSize = null, double? pageNum = null, bool? isSubscribed = null, bool? isPendingAge21Verification = null, bool? isArchiveIncluded = null)

Get opt in list subscribers by page

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
    public class FetchOptInListSubscribersByPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var pageSize = 1.2D;  // double? |  (optional) 
            var pageNum = 1.2D;  // double? |  (optional) 
            var isSubscribed = true;  // bool? |  (optional) 
            var isPendingAge21Verification = true;  // bool? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get opt in list subscribers by page
                FetchOptInListSubscribersByPage200Response result = apiInstance.FetchOptInListSubscribersByPage(listID, pageSize, pageNum, isSubscribed, isPendingAge21Verification, isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInListSubscribersByPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListSubscribersByPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get opt in list subscribers by page
    ApiResponse<FetchOptInListSubscribersByPage200Response> response = apiInstance.FetchOptInListSubscribersByPageWithHttpInfo(listID, pageSize, pageNum, isSubscribed, isPendingAge21Verification, isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInListSubscribersByPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **pageSize** | **double?** |  | [optional]  |
| **pageNum** | **double?** |  | [optional]  |
| **isSubscribed** | **bool?** |  | [optional]  |
| **isPendingAge21Verification** | **bool?** |  | [optional]  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**FetchOptInListSubscribersByPage200Response**](FetchOptInListSubscribersByPage200Response.md)

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

<a id="fetchoptinlists"></a>
# **FetchOptInLists**
> Object FetchOptInLists (bool? isArchiveIncluded = null)

Get all opt in lists

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
    public class FetchOptInListsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all opt in lists
                Object result = apiInstance.FetchOptInLists(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInLists: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all opt in lists
    ApiResponse<Object> response = apiInstance.FetchOptInListsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInListsWithHttpInfo: " + e.Message);
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

<a id="fetchoptinlistsassociatedwithphonenumber"></a>
# **FetchOptInListsAssociatedWithPhoneNumber**
> List&lt;OptInList&gt; FetchOptInListsAssociatedWithPhoneNumber (string phoneNumberID)

Get opt in lists

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
    public class FetchOptInListsAssociatedWithPhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get opt in lists
                List<OptInList> result = apiInstance.FetchOptInListsAssociatedWithPhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInListsAssociatedWithPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListsAssociatedWithPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get opt in lists
    ApiResponse<List<OptInList>> response = apiInstance.FetchOptInListsAssociatedWithPhoneNumberWithHttpInfo(phoneNumberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInListsAssociatedWithPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |

### Return type

[**List&lt;OptInList&gt;**](OptInList.md)

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

<a id="fetchoptinsourcesubscribers"></a>
# **FetchOptInSourceSubscribers**
> List&lt;OptInListSubscriber&gt; FetchOptInSourceSubscribers (string sourceID, bool? isSubscribed = null, bool? isPendingAge21Verification = null, bool? isArchiveIncluded = null)

Get opt in source subscribers

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
    public class FetchOptInSourceSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var sourceID = "sourceID_example";  // string | 
            var isSubscribed = true;  // bool? |  (optional) 
            var isPendingAge21Verification = true;  // bool? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get opt in source subscribers
                List<OptInListSubscriber> result = apiInstance.FetchOptInSourceSubscribers(sourceID, isSubscribed, isPendingAge21Verification, isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInSourceSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInSourceSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get opt in source subscribers
    ApiResponse<List<OptInListSubscriber>> response = apiInstance.FetchOptInSourceSubscribersWithHttpInfo(sourceID, isSubscribed, isPendingAge21Verification, isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInSourceSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sourceID** | **string** |  |  |
| **isSubscribed** | **bool?** |  | [optional]  |
| **isPendingAge21Verification** | **bool?** |  | [optional]  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;OptInListSubscriber&gt;**](OptInListSubscriber.md)

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

<a id="fetchoptinsourcesassociatedwithphonenumber"></a>
# **FetchOptInSourcesAssociatedWithPhoneNumber**
> List&lt;OptInListSource&gt; FetchOptInSourcesAssociatedWithPhoneNumber (string phoneNumberID)

Get opt in sources

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
    public class FetchOptInSourcesAssociatedWithPhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get opt in sources
                List<OptInListSource> result = apiInstance.FetchOptInSourcesAssociatedWithPhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.FetchOptInSourcesAssociatedWithPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInSourcesAssociatedWithPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get opt in sources
    ApiResponse<List<OptInListSource>> response = apiInstance.FetchOptInSourcesAssociatedWithPhoneNumberWithHttpInfo(phoneNumberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.FetchOptInSourcesAssociatedWithPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |

### Return type

[**List&lt;OptInListSource&gt;**](OptInListSource.md)

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

<a id="importoptinlistsubscribers"></a>
# **ImportOptInListSubscribers**
> string ImportOptInListSubscribers (string listID, WTSMSImportOptInListSubscribers wTSMSImportOptInListSubscribers)

Import opt in list subscribers

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
    public class ImportOptInListSubscribersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var wTSMSImportOptInListSubscribers = new WTSMSImportOptInListSubscribers(); // WTSMSImportOptInListSubscribers | 

            try
            {
                // Import opt in list subscribers
                string result = apiInstance.ImportOptInListSubscribers(listID, wTSMSImportOptInListSubscribers);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.ImportOptInListSubscribers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImportOptInListSubscribersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Import opt in list subscribers
    ApiResponse<string> response = apiInstance.ImportOptInListSubscribersWithHttpInfo(listID, wTSMSImportOptInListSubscribers);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.ImportOptInListSubscribersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **wTSMSImportOptInListSubscribers** | [**WTSMSImportOptInListSubscribers**](WTSMSImportOptInListSubscribers.md) |  |  |

### Return type

**string**

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

<a id="saveoptinlist"></a>
# **SaveOptInList**
> OptInList SaveOptInList (string listID, WTOptInListCreationParams wTOptInListCreationParams)

Save opt in list

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
    public class SaveOptInListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var wTOptInListCreationParams = new WTOptInListCreationParams(); // WTOptInListCreationParams | 

            try
            {
                // Save opt in list
                OptInList result = apiInstance.SaveOptInList(listID, wTOptInListCreationParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.SaveOptInList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveOptInListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Save opt in list
    ApiResponse<OptInList> response = apiInstance.SaveOptInListWithHttpInfo(listID, wTOptInListCreationParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.SaveOptInListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **wTOptInListCreationParams** | [**WTOptInListCreationParams**](WTOptInListCreationParams.md) |  |  |

### Return type

[**OptInList**](OptInList.md)

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

<a id="saveoptinlistsource"></a>
# **SaveOptInListSource**
> OptInListSource SaveOptInListSource (string sourceID, WTSMSOptInListSourceCreate wTSMSOptInListSourceCreate)

Save opt in list source

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
    public class SaveOptInListSourceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new OptInListsApi(httpClient, config, httpClientHandler);
            var sourceID = "sourceID_example";  // string | 
            var wTSMSOptInListSourceCreate = new WTSMSOptInListSourceCreate(); // WTSMSOptInListSourceCreate | 

            try
            {
                // Save opt in list source
                OptInListSource result = apiInstance.SaveOptInListSource(sourceID, wTSMSOptInListSourceCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OptInListsApi.SaveOptInListSource: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveOptInListSourceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Save opt in list source
    ApiResponse<OptInListSource> response = apiInstance.SaveOptInListSourceWithHttpInfo(sourceID, wTSMSOptInListSourceCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OptInListsApi.SaveOptInListSourceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sourceID** | **string** |  |  |
| **wTSMSOptInListSourceCreate** | [**WTSMSOptInListSourceCreate**](WTSMSOptInListSourceCreate.md) |  |  |

### Return type

[**OptInListSource**](OptInListSource.md)

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

