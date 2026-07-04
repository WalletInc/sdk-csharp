# WalletInc.Api.HelpDeskApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchHelpDeskRequests**](HelpDeskApi.md#fetchhelpdeskrequests) | **GET** /v2/merchant/helpDeskRequests/{phoneNumberID} | Get help desk requests |
| [**SendHelpDeskResponse**](HelpDeskApi.md#sendhelpdeskresponse) | **POST** /v2/employee/helpDesk/response | Send help desk response |
| [**SetHelpDeskRequestResolved**](HelpDeskApi.md#sethelpdeskrequestresolved) | **PATCH** /v2/employee/helpDesk/request/{helpDeskRequestID} | Resolve help desk request |

<a id="fetchhelpdeskrequests"></a>
# **FetchHelpDeskRequests**
> List&lt;HelpDeskRequest&gt; FetchHelpDeskRequests (string phoneNumberID, bool? isResolved = null)

Get help desk requests

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
    public class FetchHelpDeskRequestsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new HelpDeskApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var isResolved = true;  // bool? |  (optional) 

            try
            {
                // Get help desk requests
                List<HelpDeskRequest> result = apiInstance.FetchHelpDeskRequests(phoneNumberID, isResolved);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling HelpDeskApi.FetchHelpDeskRequests: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchHelpDeskRequestsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get help desk requests
    ApiResponse<List<HelpDeskRequest>> response = apiInstance.FetchHelpDeskRequestsWithHttpInfo(phoneNumberID, isResolved);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling HelpDeskApi.FetchHelpDeskRequestsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **isResolved** | **bool?** |  | [optional]  |

### Return type

[**List&lt;HelpDeskRequest&gt;**](HelpDeskRequest.md)

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

<a id="sendhelpdeskresponse"></a>
# **SendHelpDeskResponse**
> OutboundSMS SendHelpDeskResponse (WTEmployeeSendHelpDeskResponse wTEmployeeSendHelpDeskResponse)

Send help desk response

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
    public class SendHelpDeskResponseExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new HelpDeskApi(httpClient, config, httpClientHandler);
            var wTEmployeeSendHelpDeskResponse = new WTEmployeeSendHelpDeskResponse(); // WTEmployeeSendHelpDeskResponse | 

            try
            {
                // Send help desk response
                OutboundSMS result = apiInstance.SendHelpDeskResponse(wTEmployeeSendHelpDeskResponse);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling HelpDeskApi.SendHelpDeskResponse: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendHelpDeskResponseWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send help desk response
    ApiResponse<OutboundSMS> response = apiInstance.SendHelpDeskResponseWithHttpInfo(wTEmployeeSendHelpDeskResponse);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling HelpDeskApi.SendHelpDeskResponseWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeSendHelpDeskResponse** | [**WTEmployeeSendHelpDeskResponse**](WTEmployeeSendHelpDeskResponse.md) |  |  |

### Return type

[**OutboundSMS**](OutboundSMS.md)

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

<a id="sethelpdeskrequestresolved"></a>
# **SetHelpDeskRequestResolved**
> HelpDeskRequest SetHelpDeskRequestResolved (string helpDeskRequestID)

Resolve help desk request

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
    public class SetHelpDeskRequestResolvedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new HelpDeskApi(httpClient, config, httpClientHandler);
            var helpDeskRequestID = "helpDeskRequestID_example";  // string | 

            try
            {
                // Resolve help desk request
                HelpDeskRequest result = apiInstance.SetHelpDeskRequestResolved(helpDeskRequestID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling HelpDeskApi.SetHelpDeskRequestResolved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetHelpDeskRequestResolvedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resolve help desk request
    ApiResponse<HelpDeskRequest> response = apiInstance.SetHelpDeskRequestResolvedWithHttpInfo(helpDeskRequestID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling HelpDeskApi.SetHelpDeskRequestResolvedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **helpDeskRequestID** | **string** |  |  |

### Return type

[**HelpDeskRequest**](HelpDeskRequest.md)

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

