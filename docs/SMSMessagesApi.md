# WalletInc.Api.SMSMessagesApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CountInboundSMS**](SMSMessagesApi.md#countinboundsms) | **GET** /v2/merchant/sms/inbound/count/{phoneNumberID} | Count inbound SMSes |
| [**CountOutboundSMS**](SMSMessagesApi.md#countoutboundsms) | **GET** /v2/sms/outbound/count/{phoneNumberID} | Count outbound SMS |
| [**EstimateSMSSegments**](SMSMessagesApi.md#estimatesmssegments) | **POST** /sms/segment-estimate | Estimate SMS/MMS segments for a message |
| [**ExportInboundMessages**](SMSMessagesApi.md#exportinboundmessages) | **PUT** /v2/merchant/sms/inbound/export/{phoneNumberID} | Export inbound messages |
| [**ExportOutboundMessages**](SMSMessagesApi.md#exportoutboundmessages) | **PUT** /v2/merchant/sms/outbound/export/{phoneNumberID} | Export outbound messages |
| [**FetchInboundSMS**](SMSMessagesApi.md#fetchinboundsms) | **GET** /v2/merchant/sms/inbound/{phoneNumberID} | Get inbound SMSes |
| [**FetchInboundSMSByPage**](SMSMessagesApi.md#fetchinboundsmsbypage) | **GET** /v2/merchant/sms/inbound/page/{phoneNumberID} | Get inbound SMSes by page |
| [**FetchMerchantOutboundSMS**](SMSMessagesApi.md#fetchmerchantoutboundsms) | **GET** /v2/merchant/sms/outbound/{phoneNumberID} | Get outbound SMSes |
| [**FetchOutboundSMS**](SMSMessagesApi.md#fetchoutboundsms) | **GET** /v2/sms/outbound/{phoneNumberID} | Get outbound SMS |
| [**FetchOutboundSMSByPage**](SMSMessagesApi.md#fetchoutboundsmsbypage) | **GET** /v2/sms/outbound/page/{phoneNumberID} | Get outbound SMSes by page |
| [**RetrieveSentAndMaxCountOfMessages**](SMSMessagesApi.md#retrievesentandmaxcountofmessages) | **GET** /v2/sms/sent | Retrieve the number of messages sent by the merchant within the current billing cycle |

<a id="countinboundsms"></a>
# **CountInboundSMS**
> WTCountResult CountInboundSMS (string phoneNumberID, string? fromPhoneNumber = null, string? body = null, DateTime? startDate = null, DateTime? endDate = null)

Count inbound SMSes

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
    public class CountInboundSMSExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var fromPhoneNumber = "fromPhoneNumber_example";  // string? |  (optional) 
            var body = "body_example";  // string? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count inbound SMSes
                WTCountResult result = apiInstance.CountInboundSMS(phoneNumberID, fromPhoneNumber, body, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.CountInboundSMS: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountInboundSMSWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count inbound SMSes
    ApiResponse<WTCountResult> response = apiInstance.CountInboundSMSWithHttpInfo(phoneNumberID, fromPhoneNumber, body, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.CountInboundSMSWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **fromPhoneNumber** | **string?** |  | [optional]  |
| **body** | **string?** |  | [optional]  |
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

<a id="countoutboundsms"></a>
# **CountOutboundSMS**
> WTCountResult CountOutboundSMS (string phoneNumberID, string? toPhoneNumber = null, string? status = null, string? paymentObjectBroadcastID = null, DateTime? startDate = null, DateTime? endDate = null)

Count outbound SMS

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
    public class CountOutboundSMSExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var toPhoneNumber = "toPhoneNumber_example";  // string? |  (optional) 
            var status = "status_example";  // string? |  (optional) 
            var paymentObjectBroadcastID = "paymentObjectBroadcastID_example";  // string? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count outbound SMS
                WTCountResult result = apiInstance.CountOutboundSMS(phoneNumberID, toPhoneNumber, status, paymentObjectBroadcastID, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.CountOutboundSMS: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountOutboundSMSWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count outbound SMS
    ApiResponse<WTCountResult> response = apiInstance.CountOutboundSMSWithHttpInfo(phoneNumberID, toPhoneNumber, status, paymentObjectBroadcastID, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.CountOutboundSMSWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **toPhoneNumber** | **string?** |  | [optional]  |
| **status** | **string?** |  | [optional]  |
| **paymentObjectBroadcastID** | **string?** |  | [optional]  |
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

<a id="estimatesmssegments"></a>
# **EstimateSMSSegments**
> WTSegmentEstimate EstimateSMSSegments (WTSegmentEstimateRequest wTSegmentEstimateRequest)

Estimate SMS/MMS segments for a message

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
    public class EstimateSMSSegmentsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var wTSegmentEstimateRequest = new WTSegmentEstimateRequest(); // WTSegmentEstimateRequest | 

            try
            {
                // Estimate SMS/MMS segments for a message
                WTSegmentEstimate result = apiInstance.EstimateSMSSegments(wTSegmentEstimateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.EstimateSMSSegments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EstimateSMSSegmentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Estimate SMS/MMS segments for a message
    ApiResponse<WTSegmentEstimate> response = apiInstance.EstimateSMSSegmentsWithHttpInfo(wTSegmentEstimateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.EstimateSMSSegmentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTSegmentEstimateRequest** | [**WTSegmentEstimateRequest**](WTSegmentEstimateRequest.md) |  |  |

### Return type

[**WTSegmentEstimate**](WTSegmentEstimate.md)

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

<a id="exportinboundmessages"></a>
# **ExportInboundMessages**
> string ExportInboundMessages (string phoneNumberID, string locale)

Export inbound messages

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
    public class ExportInboundMessagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var locale = "locale_example";  // string | 

            try
            {
                // Export inbound messages
                string result = apiInstance.ExportInboundMessages(phoneNumberID, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.ExportInboundMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportInboundMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export inbound messages
    ApiResponse<string> response = apiInstance.ExportInboundMessagesWithHttpInfo(phoneNumberID, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.ExportInboundMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **locale** | **string** |  |  |

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

<a id="exportoutboundmessages"></a>
# **ExportOutboundMessages**
> string ExportOutboundMessages (string phoneNumberID, string locale, string? paymentObjectBroadcastID = null)

Export outbound messages

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
    public class ExportOutboundMessagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var locale = "locale_example";  // string | 
            var paymentObjectBroadcastID = "paymentObjectBroadcastID_example";  // string? |  (optional) 

            try
            {
                // Export outbound messages
                string result = apiInstance.ExportOutboundMessages(phoneNumberID, locale, paymentObjectBroadcastID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.ExportOutboundMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportOutboundMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export outbound messages
    ApiResponse<string> response = apiInstance.ExportOutboundMessagesWithHttpInfo(phoneNumberID, locale, paymentObjectBroadcastID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.ExportOutboundMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **locale** | **string** |  |  |
| **paymentObjectBroadcastID** | **string?** |  | [optional]  |

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

<a id="fetchinboundsms"></a>
# **FetchInboundSMS**
> List&lt;InboundSMS&gt; FetchInboundSMS (string phoneNumberID, string? fromPhoneNumber = null)

Get inbound SMSes

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
    public class FetchInboundSMSExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var fromPhoneNumber = "fromPhoneNumber_example";  // string? |  (optional) 

            try
            {
                // Get inbound SMSes
                List<InboundSMS> result = apiInstance.FetchInboundSMS(phoneNumberID, fromPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.FetchInboundSMS: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInboundSMSWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get inbound SMSes
    ApiResponse<List<InboundSMS>> response = apiInstance.FetchInboundSMSWithHttpInfo(phoneNumberID, fromPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.FetchInboundSMSWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **fromPhoneNumber** | **string?** |  | [optional]  |

### Return type

[**List&lt;InboundSMS&gt;**](InboundSMS.md)

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

<a id="fetchinboundsmsbypage"></a>
# **FetchInboundSMSByPage**
> FetchInboundSMSByPage200Response FetchInboundSMSByPage (string phoneNumberID, string? fromPhoneNumber = null, double? pageSize = null, double? pageNum = null, DateTime? startDate = null, DateTime? endDate = null)

Get inbound SMSes by page

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
    public class FetchInboundSMSByPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var fromPhoneNumber = "fromPhoneNumber_example";  // string? |  (optional) 
            var pageSize = 1.2D;  // double? |  (optional) 
            var pageNum = 1.2D;  // double? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get inbound SMSes by page
                FetchInboundSMSByPage200Response result = apiInstance.FetchInboundSMSByPage(phoneNumberID, fromPhoneNumber, pageSize, pageNum, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.FetchInboundSMSByPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInboundSMSByPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get inbound SMSes by page
    ApiResponse<FetchInboundSMSByPage200Response> response = apiInstance.FetchInboundSMSByPageWithHttpInfo(phoneNumberID, fromPhoneNumber, pageSize, pageNum, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.FetchInboundSMSByPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **fromPhoneNumber** | **string?** |  | [optional]  |
| **pageSize** | **double?** |  | [optional]  |
| **pageNum** | **double?** |  | [optional]  |
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

[**FetchInboundSMSByPage200Response**](FetchInboundSMSByPage200Response.md)

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

<a id="fetchmerchantoutboundsms"></a>
# **FetchMerchantOutboundSMS**
> List&lt;OutboundSMS&gt; FetchMerchantOutboundSMS (string phoneNumberID, string toPhoneNumber)

Get outbound SMSes

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
    public class FetchMerchantOutboundSMSExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var toPhoneNumber = "toPhoneNumber_example";  // string | 

            try
            {
                // Get outbound SMSes
                List<OutboundSMS> result = apiInstance.FetchMerchantOutboundSMS(phoneNumberID, toPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.FetchMerchantOutboundSMS: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMerchantOutboundSMSWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get outbound SMSes
    ApiResponse<List<OutboundSMS>> response = apiInstance.FetchMerchantOutboundSMSWithHttpInfo(phoneNumberID, toPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.FetchMerchantOutboundSMSWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **toPhoneNumber** | **string** |  |  |

### Return type

[**List&lt;OutboundSMS&gt;**](OutboundSMS.md)

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

<a id="fetchoutboundsms"></a>
# **FetchOutboundSMS**
> List&lt;OutboundSMS&gt; FetchOutboundSMS (string phoneNumberID, string? toPhoneNumber = null, string? status = null, string? paymentObjectBroadcastID = null)

Get outbound SMS

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
    public class FetchOutboundSMSExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var toPhoneNumber = "toPhoneNumber_example";  // string? |  (optional) 
            var status = "status_example";  // string? |  (optional) 
            var paymentObjectBroadcastID = "paymentObjectBroadcastID_example";  // string? |  (optional) 

            try
            {
                // Get outbound SMS
                List<OutboundSMS> result = apiInstance.FetchOutboundSMS(phoneNumberID, toPhoneNumber, status, paymentObjectBroadcastID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.FetchOutboundSMS: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOutboundSMSWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get outbound SMS
    ApiResponse<List<OutboundSMS>> response = apiInstance.FetchOutboundSMSWithHttpInfo(phoneNumberID, toPhoneNumber, status, paymentObjectBroadcastID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.FetchOutboundSMSWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **toPhoneNumber** | **string?** |  | [optional]  |
| **status** | **string?** |  | [optional]  |
| **paymentObjectBroadcastID** | **string?** |  | [optional]  |

### Return type

[**List&lt;OutboundSMS&gt;**](OutboundSMS.md)

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

<a id="fetchoutboundsmsbypage"></a>
# **FetchOutboundSMSByPage**
> FetchOutboundSMSByPage200Response FetchOutboundSMSByPage (string phoneNumberID, string? toPhoneNumber = null, string? paymentObjectBroadcastID = null, double? pageSize = null, double? pageNum = null, SSOutboundStatuses? status = null, DateTime? startDate = null, DateTime? endDate = null)

Get outbound SMSes by page

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
    public class FetchOutboundSMSByPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var toPhoneNumber = "toPhoneNumber_example";  // string? |  (optional) 
            var paymentObjectBroadcastID = "paymentObjectBroadcastID_example";  // string? |  (optional) 
            var pageSize = 1.2D;  // double? |  (optional) 
            var pageNum = 1.2D;  // double? |  (optional) 
            var status = new SSOutboundStatuses?(); // SSOutboundStatuses? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Get outbound SMSes by page
                FetchOutboundSMSByPage200Response result = apiInstance.FetchOutboundSMSByPage(phoneNumberID, toPhoneNumber, paymentObjectBroadcastID, pageSize, pageNum, status, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.FetchOutboundSMSByPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOutboundSMSByPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get outbound SMSes by page
    ApiResponse<FetchOutboundSMSByPage200Response> response = apiInstance.FetchOutboundSMSByPageWithHttpInfo(phoneNumberID, toPhoneNumber, paymentObjectBroadcastID, pageSize, pageNum, status, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.FetchOutboundSMSByPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **toPhoneNumber** | **string?** |  | [optional]  |
| **paymentObjectBroadcastID** | **string?** |  | [optional]  |
| **pageSize** | **double?** |  | [optional]  |
| **pageNum** | **double?** |  | [optional]  |
| **status** | [**SSOutboundStatuses?**](SSOutboundStatuses?.md) |  | [optional]  |
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

[**FetchOutboundSMSByPage200Response**](FetchOutboundSMSByPage200Response.md)

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

<a id="retrievesentandmaxcountofmessages"></a>
# **RetrieveSentAndMaxCountOfMessages**
> Object RetrieveSentAndMaxCountOfMessages ()

Retrieve the number of messages sent by the merchant within the current billing cycle

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
    public class RetrieveSentAndMaxCountOfMessagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSMessagesApi(httpClient, config, httpClientHandler);

            try
            {
                // Retrieve the number of messages sent by the merchant within the current billing cycle
                Object result = apiInstance.RetrieveSentAndMaxCountOfMessages();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSMessagesApi.RetrieveSentAndMaxCountOfMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RetrieveSentAndMaxCountOfMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve the number of messages sent by the merchant within the current billing cycle
    ApiResponse<Object> response = apiInstance.RetrieveSentAndMaxCountOfMessagesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSMessagesApi.RetrieveSentAndMaxCountOfMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
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

