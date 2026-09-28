# WalletInc.Api.KeywordAutoRespondersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveAutoResponder**](KeywordAutoRespondersApi.md#archiveautoresponder) | **POST** /autoresponders/archive/{autoResponderID} | Archive a keyword auto-responder |
| [**CreateAutoResponder**](KeywordAutoRespondersApi.md#createautoresponder) | **POST** /autoresponders/create | Create a keyword auto-responder |
| [**FetchAllAutoResponders**](KeywordAutoRespondersApi.md#fetchallautoresponders) | **GET** /autoresponders/fetchAll | List keyword auto-responders |
| [**FetchAutoResponderHits**](KeywordAutoRespondersApi.md#fetchautoresponderhits) | **GET** /autoresponders/hits | List keyword auto-responder activity |
| [**RestoreAutoResponder**](KeywordAutoRespondersApi.md#restoreautoresponder) | **POST** /autoresponders/restore/{autoResponderID} | Restore a keyword auto-responder |
| [**UpdateAutoResponder**](KeywordAutoRespondersApi.md#updateautoresponder) | **POST** /autoresponders/update | Update a keyword auto-responder |

<a id="archiveautoresponder"></a>
# **ArchiveAutoResponder**
> WTAutoResponder ArchiveAutoResponder (string autoResponderID)

Archive a keyword auto-responder

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
    public class ArchiveAutoResponderExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new KeywordAutoRespondersApi(httpClient, config, httpClientHandler);
            var autoResponderID = "autoResponderID_example";  // string | 

            try
            {
                // Archive a keyword auto-responder
                WTAutoResponder result = apiInstance.ArchiveAutoResponder(autoResponderID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling KeywordAutoRespondersApi.ArchiveAutoResponder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveAutoResponderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive a keyword auto-responder
    ApiResponse<WTAutoResponder> response = apiInstance.ArchiveAutoResponderWithHttpInfo(autoResponderID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling KeywordAutoRespondersApi.ArchiveAutoResponderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **autoResponderID** | **string** |  |  |

### Return type

[**WTAutoResponder**](WTAutoResponder.md)

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
| **422** | Validation Failed. A refused keyword names the rule it broke in the failing field&#39;s message: reserved-compliance-keyword, opt-out-phrase, date-shaped, help-desk-keyword, opt-in-list-keyword (with a listID field), duplicate (with an existingID field), empty, too-long, or empty-response (on responseBody). |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createautoresponder"></a>
# **CreateAutoResponder**
> WTAutoResponder CreateAutoResponder (WTAutoResponderCreateParams wTAutoResponderCreateParams)

Create a keyword auto-responder

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
    public class CreateAutoResponderExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new KeywordAutoRespondersApi(httpClient, config, httpClientHandler);
            var wTAutoResponderCreateParams = new WTAutoResponderCreateParams(); // WTAutoResponderCreateParams | 

            try
            {
                // Create a keyword auto-responder
                WTAutoResponder result = apiInstance.CreateAutoResponder(wTAutoResponderCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling KeywordAutoRespondersApi.CreateAutoResponder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAutoResponderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a keyword auto-responder
    ApiResponse<WTAutoResponder> response = apiInstance.CreateAutoResponderWithHttpInfo(wTAutoResponderCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling KeywordAutoRespondersApi.CreateAutoResponderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTAutoResponderCreateParams** | [**WTAutoResponderCreateParams**](WTAutoResponderCreateParams.md) |  |  |

### Return type

[**WTAutoResponder**](WTAutoResponder.md)

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
| **422** | Validation Failed. A refused keyword names the rule it broke in the failing field&#39;s message: reserved-compliance-keyword, opt-out-phrase, date-shaped, help-desk-keyword, opt-in-list-keyword (with a listID field), duplicate (with an existingID field), empty, too-long, or empty-response (on responseBody). |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchallautoresponders"></a>
# **FetchAllAutoResponders**
> List&lt;WTAutoResponder&gt; FetchAllAutoResponders (string? phoneNumberID = null, bool? isArchiveIncluded = null)

List keyword auto-responders

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
    public class FetchAllAutoRespondersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new KeywordAutoRespondersApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // List keyword auto-responders
                List<WTAutoResponder> result = apiInstance.FetchAllAutoResponders(phoneNumberID, isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling KeywordAutoRespondersApi.FetchAllAutoResponders: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllAutoRespondersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List keyword auto-responders
    ApiResponse<List<WTAutoResponder>> response = apiInstance.FetchAllAutoRespondersWithHttpInfo(phoneNumberID, isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling KeywordAutoRespondersApi.FetchAllAutoRespondersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string?** |  | [optional]  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;WTAutoResponder&gt;**](WTAutoResponder.md)

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
| **422** | Validation Failed. A refused keyword names the rule it broke in the failing field&#39;s message: reserved-compliance-keyword, opt-out-phrase, date-shaped, help-desk-keyword, opt-in-list-keyword (with a listID field), duplicate (with an existingID field), empty, too-long, or empty-response (on responseBody). |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchautoresponderhits"></a>
# **FetchAutoResponderHits**
> List&lt;WTAutoResponderHit&gt; FetchAutoResponderHits (string? autoResponderID = null, int? limit = null, int? offset = null)

List keyword auto-responder activity

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
    public class FetchAutoResponderHitsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new KeywordAutoRespondersApi(httpClient, config, httpClientHandler);
            var autoResponderID = "autoResponderID_example";  // string? |  (optional) 
            var limit = 56;  // int? | Maximum number of records to return (optional) 
            var offset = 56;  // int? | Number of records to skip (optional) 

            try
            {
                // List keyword auto-responder activity
                List<WTAutoResponderHit> result = apiInstance.FetchAutoResponderHits(autoResponderID, limit, offset);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling KeywordAutoRespondersApi.FetchAutoResponderHits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAutoResponderHitsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List keyword auto-responder activity
    ApiResponse<List<WTAutoResponderHit>> response = apiInstance.FetchAutoResponderHitsWithHttpInfo(autoResponderID, limit, offset);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling KeywordAutoRespondersApi.FetchAutoResponderHitsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **autoResponderID** | **string?** |  | [optional]  |
| **limit** | **int?** | Maximum number of records to return | [optional]  |
| **offset** | **int?** | Number of records to skip | [optional]  |

### Return type

[**List&lt;WTAutoResponderHit&gt;**](WTAutoResponderHit.md)

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
| **422** | Validation Failed. A refused keyword names the rule it broke in the failing field&#39;s message: reserved-compliance-keyword, opt-out-phrase, date-shaped, help-desk-keyword, opt-in-list-keyword (with a listID field), duplicate (with an existingID field), empty, too-long, or empty-response (on responseBody). |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="restoreautoresponder"></a>
# **RestoreAutoResponder**
> WTAutoResponder RestoreAutoResponder (string autoResponderID)

Restore a keyword auto-responder

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
    public class RestoreAutoResponderExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new KeywordAutoRespondersApi(httpClient, config, httpClientHandler);
            var autoResponderID = "autoResponderID_example";  // string | 

            try
            {
                // Restore a keyword auto-responder
                WTAutoResponder result = apiInstance.RestoreAutoResponder(autoResponderID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling KeywordAutoRespondersApi.RestoreAutoResponder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreAutoResponderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore a keyword auto-responder
    ApiResponse<WTAutoResponder> response = apiInstance.RestoreAutoResponderWithHttpInfo(autoResponderID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling KeywordAutoRespondersApi.RestoreAutoResponderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **autoResponderID** | **string** |  |  |

### Return type

[**WTAutoResponder**](WTAutoResponder.md)

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
| **422** | Validation Failed. A refused keyword names the rule it broke in the failing field&#39;s message: reserved-compliance-keyword, opt-out-phrase, date-shaped, help-desk-keyword, opt-in-list-keyword (with a listID field), duplicate (with an existingID field), empty, too-long, or empty-response (on responseBody). |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updateautoresponder"></a>
# **UpdateAutoResponder**
> WTAutoResponder UpdateAutoResponder (WTAutoResponderUpdateParams wTAutoResponderUpdateParams)

Update a keyword auto-responder

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
    public class UpdateAutoResponderExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new KeywordAutoRespondersApi(httpClient, config, httpClientHandler);
            var wTAutoResponderUpdateParams = new WTAutoResponderUpdateParams(); // WTAutoResponderUpdateParams | 

            try
            {
                // Update a keyword auto-responder
                WTAutoResponder result = apiInstance.UpdateAutoResponder(wTAutoResponderUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling KeywordAutoRespondersApi.UpdateAutoResponder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAutoResponderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update a keyword auto-responder
    ApiResponse<WTAutoResponder> response = apiInstance.UpdateAutoResponderWithHttpInfo(wTAutoResponderUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling KeywordAutoRespondersApi.UpdateAutoResponderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTAutoResponderUpdateParams** | [**WTAutoResponderUpdateParams**](WTAutoResponderUpdateParams.md) |  |  |

### Return type

[**WTAutoResponder**](WTAutoResponder.md)

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
| **422** | Validation Failed. A refused keyword names the rule it broke in the failing field&#39;s message: reserved-compliance-keyword, opt-out-phrase, date-shaped, help-desk-keyword, opt-in-list-keyword (with a listID field), duplicate (with an existingID field), empty, too-long, or empty-response (on responseBody). |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

