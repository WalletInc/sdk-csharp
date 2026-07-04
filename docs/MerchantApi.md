# WalletInc.Api.MerchantApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveMerchantProfile**](MerchantApi.md#archivemerchantprofile) | **DELETE** /v2/merchant/delete | Archive Merchant |
| [**ArchivePaymentObjectBroadcast**](MerchantApi.md#archivepaymentobjectbroadcast) | **DELETE** /v2/merchant/paymentObjectBroadcast/{broadcastID} | Archive payment object broadcast |
| [**CountInboundSMS**](MerchantApi.md#countinboundsms) | **GET** /v2/merchant/sms/inbound/count/{phoneNumberID} | Count inbound SMSes |
| [**ExportInboundMessages**](MerchantApi.md#exportinboundmessages) | **PUT** /v2/merchant/sms/inbound/export/{phoneNumberID} | Export inbound messages |
| [**ExportOutboundMessages**](MerchantApi.md#exportoutboundmessages) | **PUT** /v2/merchant/sms/outbound/export/{phoneNumberID} | Export outbound messages |
| [**FetchAdvertisementCreditBroadcasts**](MerchantApi.md#fetchadvertisementcreditbroadcasts) | **GET** /v2/merchant/broadcasts/adCredits/all | Get all ad credit broadcasts |
| [**FetchCustomRoles**](MerchantApi.md#fetchcustomroles) | **GET** /v2/merchant/roles/custom | Get custom roles |
| [**FetchDynamicVoucherBroadcasts**](MerchantApi.md#fetchdynamicvoucherbroadcasts) | **GET** /v2/merchant/broadcasts/dynamicVouchers/all | Get all dynamic voucher broadcasts |
| [**FetchEmployees**](MerchantApi.md#fetchemployees) | **GET** /v2/merchant/employees/all | Get all employees |
| [**FetchHelpDeskRequests**](MerchantApi.md#fetchhelpdeskrequests) | **GET** /v2/merchant/helpDeskRequests/{phoneNumberID} | Get help desk requests |
| [**FetchImportedList**](MerchantApi.md#fetchimportedlist) | **GET** /v2/merchant/lists/imported/{listID} | Get imported list |
| [**FetchImportedLists**](MerchantApi.md#fetchimportedlists) | **GET** /v2/merchant/lists/imported/all | Get all imported lists |
| [**FetchInboundSMS**](MerchantApi.md#fetchinboundsms) | **GET** /v2/merchant/sms/inbound/{phoneNumberID} | Get inbound SMSes |
| [**FetchInboundSMSByPage**](MerchantApi.md#fetchinboundsmsbypage) | **GET** /v2/merchant/sms/inbound/page/{phoneNumberID} | Get inbound SMSes by page |
| [**FetchMerchantOutboundSMS**](MerchantApi.md#fetchmerchantoutboundsms) | **GET** /v2/merchant/sms/outbound/{phoneNumberID} | Get outbound SMSes |
| [**FetchMerchantPhoneNumbers**](MerchantApi.md#fetchmerchantphonenumbers) | **GET** /v2/merchant/phoneNumbers/all | Get all phone numbers |
| [**FetchOptInList**](MerchantApi.md#fetchoptinlist) | **GET** /v2/merchant/lists/optIn/{listID} | Get opt in list |
| [**FetchOptInLists**](MerchantApi.md#fetchoptinlists) | **GET** /v2/merchant/lists/optIn/all | Get all opt in lists |
| [**FetchPhoneNumber**](MerchantApi.md#fetchphonenumber) | **GET** /v2/merchant/phoneNumber/{phoneNumberID} | Get phone number |
| [**FetchPublicEmployees**](MerchantApi.md#fetchpublicemployees) | **GET** /v2/merchant/employees/public | Get public representative employees of the merchant |
| [**FetchSimpleSMSBroadcasts**](MerchantApi.md#fetchsimplesmsbroadcasts) | **GET** /v2/merchant/broadcasts/simpleSMS/all | Get all simple SMS broadcasts |
| [**FetchStaticVoucherCampaignBroadcasts**](MerchantApi.md#fetchstaticvouchercampaignbroadcasts) | **GET** /v2/merchant/broadcasts/staticVoucherCampaign/all | Get all static voucher campaign broadcasts |
| [**FetchTCPAFilter**](MerchantApi.md#fetchtcpafilter) | **GET** /v2/merchant/tcpa/filter/all | Get all TCPA Filters |
| [**FetchWalletConfiguration**](MerchantApi.md#fetchwalletconfiguration) | **GET** /v2/merchant/wallet/configuration | Get wallet configuration |
| [**UpdateMerchant**](MerchantApi.md#updatemerchant) | **PUT** /v2/merchant | Update merchant details |
| [**UpdatePointsOfContact**](MerchantApi.md#updatepointsofcontact) | **PUT** /v2/merchant/pointsOfContact | Update points of contact |
| [**UpdatePosIntegration**](MerchantApi.md#updateposintegration) | **PUT** /v2/merchant/pos/integration | Update POS Integration |

<a id="archivemerchantprofile"></a>
# **ArchiveMerchantProfile**
> Object ArchiveMerchantProfile ()

Archive Merchant

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
    public class ArchiveMerchantProfileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);

            try
            {
                // Archive Merchant
                Object result = apiInstance.ArchiveMerchantProfile();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.ArchiveMerchantProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveMerchantProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Merchant
    ApiResponse<Object> response = apiInstance.ArchiveMerchantProfileWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.ArchiveMerchantProfileWithHttpInfo: " + e.Message);
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

<a id="archivepaymentobjectbroadcast"></a>
# **ArchivePaymentObjectBroadcast**
> Object ArchivePaymentObjectBroadcast (string broadcastID)

Archive payment object broadcast

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
    public class ArchivePaymentObjectBroadcastExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var broadcastID = "broadcastID_example";  // string | 

            try
            {
                // Archive payment object broadcast
                Object result = apiInstance.ArchivePaymentObjectBroadcast(broadcastID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.ArchivePaymentObjectBroadcast: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchivePaymentObjectBroadcastWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive payment object broadcast
    ApiResponse<Object> response = apiInstance.ArchivePaymentObjectBroadcastWithHttpInfo(broadcastID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.ArchivePaymentObjectBroadcastWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **broadcastID** | **string** |  |  |

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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling MerchantApi.CountInboundSMS: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.CountInboundSMSWithHttpInfo: " + e.Message);
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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling MerchantApi.ExportInboundMessages: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.ExportInboundMessagesWithHttpInfo: " + e.Message);
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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling MerchantApi.ExportOutboundMessages: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.ExportOutboundMessagesWithHttpInfo: " + e.Message);
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

<a id="fetchadvertisementcreditbroadcasts"></a>
# **FetchAdvertisementCreditBroadcasts**
> List&lt;AdvertisementCreditBroadcast&gt; FetchAdvertisementCreditBroadcasts (bool? isArchiveIncluded = null)

Get all ad credit broadcasts

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
    public class FetchAdvertisementCreditBroadcastsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all ad credit broadcasts
                List<AdvertisementCreditBroadcast> result = apiInstance.FetchAdvertisementCreditBroadcasts(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchAdvertisementCreditBroadcasts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAdvertisementCreditBroadcastsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all ad credit broadcasts
    ApiResponse<List<AdvertisementCreditBroadcast>> response = apiInstance.FetchAdvertisementCreditBroadcastsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchAdvertisementCreditBroadcastsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;AdvertisementCreditBroadcast&gt;**](AdvertisementCreditBroadcast.md)

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

<a id="fetchcustomroles"></a>
# **FetchCustomRoles**
> Object FetchCustomRoles ()

Get custom roles

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
    public class FetchCustomRolesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);

            try
            {
                // Get custom roles
                Object result = apiInstance.FetchCustomRoles();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchCustomRoles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchCustomRolesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get custom roles
    ApiResponse<Object> response = apiInstance.FetchCustomRolesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchCustomRolesWithHttpInfo: " + e.Message);
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

<a id="fetchdynamicvoucherbroadcasts"></a>
# **FetchDynamicVoucherBroadcasts**
> List&lt;DynamicVoucherBroadcast&gt; FetchDynamicVoucherBroadcasts (bool? isArchiveIncluded = null)

Get all dynamic voucher broadcasts

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
    public class FetchDynamicVoucherBroadcastsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all dynamic voucher broadcasts
                List<DynamicVoucherBroadcast> result = apiInstance.FetchDynamicVoucherBroadcasts(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchDynamicVoucherBroadcasts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDynamicVoucherBroadcastsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all dynamic voucher broadcasts
    ApiResponse<List<DynamicVoucherBroadcast>> response = apiInstance.FetchDynamicVoucherBroadcastsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchDynamicVoucherBroadcastsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;DynamicVoucherBroadcast&gt;**](DynamicVoucherBroadcast.md)

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

<a id="fetchemployees"></a>
# **FetchEmployees**
> Object FetchEmployees ()

Get all employees

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
    public class FetchEmployeesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);

            try
            {
                // Get all employees
                Object result = apiInstance.FetchEmployees();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchEmployees: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchEmployeesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all employees
    ApiResponse<Object> response = apiInstance.FetchEmployeesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchEmployeesWithHttpInfo: " + e.Message);
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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling MerchantApi.FetchHelpDeskRequests: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.FetchHelpDeskRequestsWithHttpInfo: " + e.Message);
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

<a id="fetchimportedlist"></a>
# **FetchImportedList**
> ImportedList FetchImportedList (string listID)

Get imported list

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
    public class FetchImportedListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 

            try
            {
                // Get imported list
                ImportedList result = apiInstance.FetchImportedList(listID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchImportedList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchImportedListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get imported list
    ApiResponse<ImportedList> response = apiInstance.FetchImportedListWithHttpInfo(listID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchImportedListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |

### Return type

[**ImportedList**](ImportedList.md)

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

<a id="fetchimportedlists"></a>
# **FetchImportedLists**
> Object FetchImportedLists (bool? isArchiveIncluded = null)

Get all imported lists

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
    public class FetchImportedListsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all imported lists
                Object result = apiInstance.FetchImportedLists(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchImportedLists: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchImportedListsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all imported lists
    ApiResponse<Object> response = apiInstance.FetchImportedListsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchImportedListsWithHttpInfo: " + e.Message);
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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling MerchantApi.FetchInboundSMS: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.FetchInboundSMSWithHttpInfo: " + e.Message);
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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling MerchantApi.FetchInboundSMSByPage: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.FetchInboundSMSByPageWithHttpInfo: " + e.Message);
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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling MerchantApi.FetchMerchantOutboundSMS: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.FetchMerchantOutboundSMSWithHttpInfo: " + e.Message);
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

<a id="fetchmerchantphonenumbers"></a>
# **FetchMerchantPhoneNumbers**
> Object FetchMerchantPhoneNumbers (bool? isArchiveIncluded = null, bool? isApproved = null)

Get all phone numbers

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
    public class FetchMerchantPhoneNumbersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 
            var isApproved = true;  // bool? |  (optional) 

            try
            {
                // Get all phone numbers
                Object result = apiInstance.FetchMerchantPhoneNumbers(isArchiveIncluded, isApproved);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchMerchantPhoneNumbers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMerchantPhoneNumbersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all phone numbers
    ApiResponse<Object> response = apiInstance.FetchMerchantPhoneNumbersWithHttpInfo(isArchiveIncluded, isApproved);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchMerchantPhoneNumbersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |
| **isApproved** | **bool?** |  | [optional]  |

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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 

            try
            {
                // Get opt in list
                OptInList result = apiInstance.FetchOptInList(listID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchOptInList: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.FetchOptInListWithHttpInfo: " + e.Message);
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
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all opt in lists
                Object result = apiInstance.FetchOptInLists(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchOptInLists: " + e.Message);
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
    Debug.Print("Exception when calling MerchantApi.FetchOptInListsWithHttpInfo: " + e.Message);
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

<a id="fetchphonenumber"></a>
# **FetchPhoneNumber**
> PhoneNumber FetchPhoneNumber (string phoneNumberID)

Get phone number

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
    public class FetchPhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get phone number
                PhoneNumber result = apiInstance.FetchPhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get phone number
    ApiResponse<PhoneNumber> response = apiInstance.FetchPhoneNumberWithHttpInfo(phoneNumberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |

### Return type

[**PhoneNumber**](PhoneNumber.md)

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

<a id="fetchpublicemployees"></a>
# **FetchPublicEmployees**
> Object FetchPublicEmployees ()

Get public representative employees of the merchant

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
    public class FetchPublicEmployeesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);

            try
            {
                // Get public representative employees of the merchant
                Object result = apiInstance.FetchPublicEmployees();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchPublicEmployees: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchPublicEmployeesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get public representative employees of the merchant
    ApiResponse<Object> response = apiInstance.FetchPublicEmployeesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchPublicEmployeesWithHttpInfo: " + e.Message);
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

<a id="fetchsimplesmsbroadcasts"></a>
# **FetchSimpleSMSBroadcasts**
> List&lt;SimpleSMSBroadcast&gt; FetchSimpleSMSBroadcasts (bool? isArchiveIncluded = null)

Get all simple SMS broadcasts

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
    public class FetchSimpleSMSBroadcastsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all simple SMS broadcasts
                List<SimpleSMSBroadcast> result = apiInstance.FetchSimpleSMSBroadcasts(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchSimpleSMSBroadcasts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchSimpleSMSBroadcastsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all simple SMS broadcasts
    ApiResponse<List<SimpleSMSBroadcast>> response = apiInstance.FetchSimpleSMSBroadcastsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchSimpleSMSBroadcastsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;SimpleSMSBroadcast&gt;**](SimpleSMSBroadcast.md)

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

<a id="fetchstaticvouchercampaignbroadcasts"></a>
# **FetchStaticVoucherCampaignBroadcasts**
> List&lt;StaticVoucherCampaignBroadcast&gt; FetchStaticVoucherCampaignBroadcasts (bool? isArchiveIncluded = null)

Get all static voucher campaign broadcasts

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
    public class FetchStaticVoucherCampaignBroadcastsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all static voucher campaign broadcasts
                List<StaticVoucherCampaignBroadcast> result = apiInstance.FetchStaticVoucherCampaignBroadcasts(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchStaticVoucherCampaignBroadcasts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchStaticVoucherCampaignBroadcastsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all static voucher campaign broadcasts
    ApiResponse<List<StaticVoucherCampaignBroadcast>> response = apiInstance.FetchStaticVoucherCampaignBroadcastsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchStaticVoucherCampaignBroadcastsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;StaticVoucherCampaignBroadcast&gt;**](StaticVoucherCampaignBroadcast.md)

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

<a id="fetchtcpafilter"></a>
# **FetchTCPAFilter**
> List&lt;Tcpa&gt; FetchTCPAFilter ()

Get all TCPA Filters

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
    public class FetchTCPAFilterExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);

            try
            {
                // Get all TCPA Filters
                List<Tcpa> result = apiInstance.FetchTCPAFilter();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchTCPAFilter: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchTCPAFilterWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all TCPA Filters
    ApiResponse<List<Tcpa>> response = apiInstance.FetchTCPAFilterWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchTCPAFilterWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;Tcpa&gt;**](Tcpa.md)

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

<a id="fetchwalletconfiguration"></a>
# **FetchWalletConfiguration**
> Object FetchWalletConfiguration ()

Get wallet configuration

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
    public class FetchWalletConfigurationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);

            try
            {
                // Get wallet configuration
                Object result = apiInstance.FetchWalletConfiguration();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.FetchWalletConfiguration: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletConfigurationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get wallet configuration
    ApiResponse<Object> response = apiInstance.FetchWalletConfigurationWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.FetchWalletConfigurationWithHttpInfo: " + e.Message);
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

<a id="updatemerchant"></a>
# **UpdateMerchant**
> Object UpdateMerchant (WTMerchantUpdate wTMerchantUpdate)

Update merchant details

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
    public class UpdateMerchantExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var wTMerchantUpdate = new WTMerchantUpdate(); // WTMerchantUpdate | 

            try
            {
                // Update merchant details
                Object result = apiInstance.UpdateMerchant(wTMerchantUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.UpdateMerchant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateMerchantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update merchant details
    ApiResponse<Object> response = apiInstance.UpdateMerchantWithHttpInfo(wTMerchantUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.UpdateMerchantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMerchantUpdate** | [**WTMerchantUpdate**](WTMerchantUpdate.md) |  |  |

### Return type

**Object**

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

<a id="updatepointsofcontact"></a>
# **UpdatePointsOfContact**
> Object UpdatePointsOfContact (WTMerchantUpdatePointsOfContact wTMerchantUpdatePointsOfContact)

Update points of contact

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
    public class UpdatePointsOfContactExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var wTMerchantUpdatePointsOfContact = new WTMerchantUpdatePointsOfContact(); // WTMerchantUpdatePointsOfContact | 

            try
            {
                // Update points of contact
                Object result = apiInstance.UpdatePointsOfContact(wTMerchantUpdatePointsOfContact);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.UpdatePointsOfContact: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdatePointsOfContactWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update points of contact
    ApiResponse<Object> response = apiInstance.UpdatePointsOfContactWithHttpInfo(wTMerchantUpdatePointsOfContact);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.UpdatePointsOfContactWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMerchantUpdatePointsOfContact** | [**WTMerchantUpdatePointsOfContact**](WTMerchantUpdatePointsOfContact.md) |  |  |

### Return type

**Object**

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

<a id="updateposintegration"></a>
# **UpdatePosIntegration**
> Object UpdatePosIntegration (WTMerchantUpdatePOSIntegration wTMerchantUpdatePOSIntegration)

Update POS Integration

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
    public class UpdatePosIntegrationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new MerchantApi(httpClient, config, httpClientHandler);
            var wTMerchantUpdatePOSIntegration = new WTMerchantUpdatePOSIntegration(); // WTMerchantUpdatePOSIntegration | 

            try
            {
                // Update POS Integration
                Object result = apiInstance.UpdatePosIntegration(wTMerchantUpdatePOSIntegration);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MerchantApi.UpdatePosIntegration: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdatePosIntegrationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update POS Integration
    ApiResponse<Object> response = apiInstance.UpdatePosIntegrationWithHttpInfo(wTMerchantUpdatePOSIntegration);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MerchantApi.UpdatePosIntegrationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMerchantUpdatePOSIntegration** | [**WTMerchantUpdatePOSIntegration**](WTMerchantUpdatePOSIntegration.md) |  |  |

### Return type

**Object**

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

