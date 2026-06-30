# WalletInc.Api.SMSOperationsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AcquirePhoneNumber**](SMSOperationsApi.md#acquirephonenumber) | **POST** /v2/sms/phoneNumber/acquire | Acquire phone number |
| [**ArchivePhoneNumber**](SMSOperationsApi.md#archivephonenumber) | **DELETE** /v2/sms/phoneNumber/{phoneNumberID} | Archive phone number |
| [**ArchiveRecipient**](SMSOperationsApi.md#archiverecipient) | **DELETE** /v2/sms/importedList/recipients/{id} | Archive recipient |
| [**CountImportedListRecipients**](SMSOperationsApi.md#countimportedlistrecipients) | **GET** /v2/sms/importedList/recipients/count/{listID} | Count imported list recipients |
| [**CountOptInListSubscribers**](SMSOperationsApi.md#countoptinlistsubscribers) | **GET** /v2/sms/optInList/subscribers/count/{listID} | Count opt in list subscribers |
| [**CountOptInSourceSubscribers**](SMSOperationsApi.md#countoptinsourcesubscribers) | **GET** /v2/sms/optInSource/subscribers/count/{sourceID} | Count opt in source subscribers |
| [**CountOutboundSMS**](SMSOperationsApi.md#countoutboundsms) | **GET** /v2/sms/outbound/count/{phoneNumberID} | Count outbound SMS |
| [**CreateImportedList**](SMSOperationsApi.md#createimportedlist) | **POST** /v2/sms/importedList | Create imported list |
| [**CreateOptInList**](SMSOperationsApi.md#createoptinlist) | **POST** /v2/sms/optInList | Create opt in list |
| [**CreateOptInListSource**](SMSOperationsApi.md#createoptinlistsource) | **POST** /v2/sms/optInListSource | Send SMS to opt in list |
| [**CreateRecipientInImportedList**](SMSOperationsApi.md#createrecipientinimportedlist) | **POST** /v2/sms/importedList/recipients/create | Add new recipient in an imported list |
| [**ExportImportedListRecipients**](SMSOperationsApi.md#exportimportedlistrecipients) | **POST** /v2/sms/importedList/recipients/export/{importedListID} | Export imported list recipients |
| [**ExportOptInListSubscribers**](SMSOperationsApi.md#exportoptinlistsubscribers) | **POST** /v2/sms/optInList/subscribers/export/{listID} | Export opt in list subscribers |
| [**FetchBlockedTCPAEntries**](SMSOperationsApi.md#fetchblockedtcpaentries) | **GET** /v2/sms/phoneNumber/blocked/{phoneNumberID} | Get blocked TCPA entries |
| [**FetchImportedListRecipients**](SMSOperationsApi.md#fetchimportedlistrecipients) | **GET** /v2/sms/importedList/recipients/{listID} | Get imported list recipients |
| [**FetchImportedListRecipientsByPage**](SMSOperationsApi.md#fetchimportedlistrecipientsbypage) | **GET** /v2/sms/importedList/recipients/page/{listID} | Get imported list recipients by page |
| [**FetchOptInListSources**](SMSOperationsApi.md#fetchoptinlistsources) | **GET** /v2/sms/optInListSources/all | Get all opt in list sources |
| [**FetchOptInListSubscribers**](SMSOperationsApi.md#fetchoptinlistsubscribers) | **GET** /v2/sms/optInList/subscribers/{listID} | Get opt in list subscribers |
| [**FetchOptInListSubscribersByPage**](SMSOperationsApi.md#fetchoptinlistsubscribersbypage) | **GET** /v2/sms/optInList/subscribers/page/{listID} | Get opt in list subscribers by page |
| [**FetchOptInListsAssociatedWithPhoneNumber**](SMSOperationsApi.md#fetchoptinlistsassociatedwithphonenumber) | **GET** /v2/sms/phoneNumber/lists/{phoneNumberID} | Get opt in lists |
| [**FetchOptInSourceSubscribers**](SMSOperationsApi.md#fetchoptinsourcesubscribers) | **GET** /v2/sms/optInSource/subscribers/{sourceID} | Get opt in source subscribers |
| [**FetchOptInSourcesAssociatedWithPhoneNumber**](SMSOperationsApi.md#fetchoptinsourcesassociatedwithphonenumber) | **GET** /v2/sms/phoneNumber/sources/{phoneNumberID} | Get opt in sources |
| [**FetchOutboundSMS**](SMSOperationsApi.md#fetchoutboundsms) | **GET** /v2/sms/outbound/{phoneNumberID} | Get outbound SMS |
| [**FetchOutboundSMSByPage**](SMSOperationsApi.md#fetchoutboundsmsbypage) | **GET** /v2/sms/outbound/page/{phoneNumberID} | Get outbound SMSes by page |
| [**FetchPaymentObjectBroadcasts**](SMSOperationsApi.md#fetchpaymentobjectbroadcasts) | **GET** /v2/sms/paymentObjectBroadcasts/{phoneNumberID} | Get payment object broadcasts |
| [**FetchSMSAgreement**](SMSOperationsApi.md#fetchsmsagreement) | **GET** /v2/sms/agreement | Get SMS Agreement |
| [**ImportImportedListRecipients**](SMSOperationsApi.md#importimportedlistrecipients) | **POST** /v2/sms/importedList/recipients/import/{importedListID} | Import imported list recipients |
| [**ImportImportedListRecipientsFromMembershipTier**](SMSOperationsApi.md#importimportedlistrecipientsfrommembershiptier) | **POST** /v2/sms/importedList/recipients/import-from-tier | Import imported list recipients from a given membership tier |
| [**ImportOptInListSubscribers**](SMSOperationsApi.md#importoptinlistsubscribers) | **POST** /v2/sms/optInList/subscribers/import/{listID} | Import opt in list subscribers |
| [**RestorePhoneNumber**](SMSOperationsApi.md#restorephonenumber) | **PATCH** /v2/sms/phoneNumber/{phoneNumberID} | Restore phone number |
| [**RestoreRecipient**](SMSOperationsApi.md#restorerecipient) | **PATCH** /v2/sms/importedList/recipients/{id} | Restore recipient |
| [**RetrieveSentAndMaxCountOfMessages**](SMSOperationsApi.md#retrievesentandmaxcountofmessages) | **GET** /v2/sms/sent | Retrieve the number of messages sent by the merchant within the current billing cycle |
| [**SaveImportedList**](SMSOperationsApi.md#saveimportedlist) | **PUT** /v2/sms/importedList/{listID} | Save imported list |
| [**SaveOptInList**](SMSOperationsApi.md#saveoptinlist) | **PUT** /v2/sms/optInList/{listID} | Save opt in list |
| [**SaveOptInListSource**](SMSOperationsApi.md#saveoptinlistsource) | **PUT** /v2/sms/optInListSource/{sourceID} | Save opt in list source |
| [**SendPhoneNumberForVerification**](SMSOperationsApi.md#sendphonenumberforverification) | **PUT** /v2/sms/phoneNumber/verification/{phoneNumberID} | Request phone number verification |
| [**UpdatePhoneNumber**](SMSOperationsApi.md#updatephonenumber) | **PUT** /v2/sms/phoneNumber/{phoneNumberID} | Update phone number |

<a id="acquirephonenumber"></a>
# **AcquirePhoneNumber**
> PhoneNumber AcquirePhoneNumber (WTSMSAcquirePhoneNumber wTSMSAcquirePhoneNumber)

Acquire phone number

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
    public class AcquirePhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var wTSMSAcquirePhoneNumber = new WTSMSAcquirePhoneNumber(); // WTSMSAcquirePhoneNumber | 

            try
            {
                // Acquire phone number
                PhoneNumber result = apiInstance.AcquirePhoneNumber(wTSMSAcquirePhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.AcquirePhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AcquirePhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Acquire phone number
    ApiResponse<PhoneNumber> response = apiInstance.AcquirePhoneNumberWithHttpInfo(wTSMSAcquirePhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.AcquirePhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTSMSAcquirePhoneNumber** | [**WTSMSAcquirePhoneNumber**](WTSMSAcquirePhoneNumber.md) |  |  |

### Return type

[**PhoneNumber**](PhoneNumber.md)

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

<a id="archivephonenumber"></a>
# **ArchivePhoneNumber**
> PhoneNumber ArchivePhoneNumber (string phoneNumberID)

Archive phone number

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
    public class ArchivePhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Archive phone number
                PhoneNumber result = apiInstance.ArchivePhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.ArchivePhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchivePhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive phone number
    ApiResponse<PhoneNumber> response = apiInstance.ArchivePhoneNumberWithHttpInfo(phoneNumberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.ArchivePhoneNumberWithHttpInfo: " + e.Message);
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

<a id="archiverecipient"></a>
# **ArchiveRecipient**
> ImportedListRecipient ArchiveRecipient (string id)

Archive recipient

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
    public class ArchiveRecipientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive recipient
                ImportedListRecipient result = apiInstance.ArchiveRecipient(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.ArchiveRecipient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveRecipientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive recipient
    ApiResponse<ImportedListRecipient> response = apiInstance.ArchiveRecipientWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.ArchiveRecipientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**ImportedListRecipient**](ImportedListRecipient.md)

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

<a id="countimportedlistrecipients"></a>
# **CountImportedListRecipients**
> WTCountResult CountImportedListRecipients (string listID, bool? isArchiveIncluded = null, DateTime? startDate = null, DateTime? endDate = null)

Count imported list recipients

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
    public class CountImportedListRecipientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var isArchiveIncluded = true;  // bool? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count imported list recipients
                WTCountResult result = apiInstance.CountImportedListRecipients(listID, isArchiveIncluded, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.CountImportedListRecipients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountImportedListRecipientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count imported list recipients
    ApiResponse<WTCountResult> response = apiInstance.CountImportedListRecipientsWithHttpInfo(listID, isArchiveIncluded, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.CountImportedListRecipientsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.CountOptInListSubscribers: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.CountOptInListSubscribersWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.CountOptInSourceSubscribers: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.CountOptInSourceSubscribersWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.CountOutboundSMS: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.CountOutboundSMSWithHttpInfo: " + e.Message);
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

<a id="createimportedlist"></a>
# **CreateImportedList**
> ImportedList CreateImportedList (WTSMSImportedListCreate wTSMSImportedListCreate)

Create imported list

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
    public class CreateImportedListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var wTSMSImportedListCreate = new WTSMSImportedListCreate(); // WTSMSImportedListCreate | 

            try
            {
                // Create imported list
                ImportedList result = apiInstance.CreateImportedList(wTSMSImportedListCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.CreateImportedList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateImportedListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create imported list
    ApiResponse<ImportedList> response = apiInstance.CreateImportedListWithHttpInfo(wTSMSImportedListCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.CreateImportedListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTSMSImportedListCreate** | [**WTSMSImportedListCreate**](WTSMSImportedListCreate.md) |  |  |

### Return type

[**ImportedList**](ImportedList.md)

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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var wTOptInListCreationParams = new WTOptInListCreationParams(); // WTOptInListCreationParams | 

            try
            {
                // Create opt in list
                OptInList result = apiInstance.CreateOptInList(wTOptInListCreationParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.CreateOptInList: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.CreateOptInListWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var wTSMSOptInListSourceCreate = new WTSMSOptInListSourceCreate(); // WTSMSOptInListSourceCreate | 

            try
            {
                // Send SMS to opt in list
                OptInListSource result = apiInstance.CreateOptInListSource(wTSMSOptInListSourceCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.CreateOptInListSource: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.CreateOptInListSourceWithHttpInfo: " + e.Message);
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

<a id="createrecipientinimportedlist"></a>
# **CreateRecipientInImportedList**
> ImportedListRecipient CreateRecipientInImportedList (SSImportedListRecipientCreateParams sSImportedListRecipientCreateParams)

Add new recipient in an imported list

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
    public class CreateRecipientInImportedListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var sSImportedListRecipientCreateParams = new SSImportedListRecipientCreateParams(); // SSImportedListRecipientCreateParams | 

            try
            {
                // Add new recipient in an imported list
                ImportedListRecipient result = apiInstance.CreateRecipientInImportedList(sSImportedListRecipientCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.CreateRecipientInImportedList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateRecipientInImportedListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add new recipient in an imported list
    ApiResponse<ImportedListRecipient> response = apiInstance.CreateRecipientInImportedListWithHttpInfo(sSImportedListRecipientCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.CreateRecipientInImportedListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sSImportedListRecipientCreateParams** | [**SSImportedListRecipientCreateParams**](SSImportedListRecipientCreateParams.md) |  |  |

### Return type

[**ImportedListRecipient**](ImportedListRecipient.md)

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

<a id="exportimportedlistrecipients"></a>
# **ExportImportedListRecipients**
> string ExportImportedListRecipients (string importedListID)

Export imported list recipients

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
    public class ExportImportedListRecipientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var importedListID = "importedListID_example";  // string | 

            try
            {
                // Export imported list recipients
                string result = apiInstance.ExportImportedListRecipients(importedListID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.ExportImportedListRecipients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportImportedListRecipientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export imported list recipients
    ApiResponse<string> response = apiInstance.ExportImportedListRecipientsWithHttpInfo(importedListID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.ExportImportedListRecipientsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **importedListID** | **string** |  |  |

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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 

            try
            {
                // Export opt in list subscribers
                string result = apiInstance.ExportOptInListSubscribers(listID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.ExportOptInListSubscribers: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.ExportOptInListSubscribersWithHttpInfo: " + e.Message);
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

<a id="fetchblockedtcpaentries"></a>
# **FetchBlockedTCPAEntries**
> List&lt;Tcpa&gt; FetchBlockedTCPAEntries (string phoneNumberID)

Get blocked TCPA entries

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
    public class FetchBlockedTCPAEntriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get blocked TCPA entries
                List<Tcpa> result = apiInstance.FetchBlockedTCPAEntries(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.FetchBlockedTCPAEntries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchBlockedTCPAEntriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get blocked TCPA entries
    ApiResponse<List<Tcpa>> response = apiInstance.FetchBlockedTCPAEntriesWithHttpInfo(phoneNumberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.FetchBlockedTCPAEntriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |

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

<a id="fetchimportedlistrecipients"></a>
# **FetchImportedListRecipients**
> List&lt;ImportedListRecipient&gt; FetchImportedListRecipients (string listID)

Get imported list recipients

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
    public class FetchImportedListRecipientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 

            try
            {
                // Get imported list recipients
                List<ImportedListRecipient> result = apiInstance.FetchImportedListRecipients(listID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.FetchImportedListRecipients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchImportedListRecipientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get imported list recipients
    ApiResponse<List<ImportedListRecipient>> response = apiInstance.FetchImportedListRecipientsWithHttpInfo(listID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.FetchImportedListRecipientsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |

### Return type

[**List&lt;ImportedListRecipient&gt;**](ImportedListRecipient.md)

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

<a id="fetchimportedlistrecipientsbypage"></a>
# **FetchImportedListRecipientsByPage**
> FetchImportedListRecipientsByPage200Response FetchImportedListRecipientsByPage (string listID, double? pageSize = null, double? pageNum = null, bool? isArchiveIncluded = null)

Get imported list recipients by page

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
    public class FetchImportedListRecipientsByPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var pageSize = 1.2D;  // double? |  (optional) 
            var pageNum = 1.2D;  // double? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get imported list recipients by page
                FetchImportedListRecipientsByPage200Response result = apiInstance.FetchImportedListRecipientsByPage(listID, pageSize, pageNum, isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.FetchImportedListRecipientsByPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchImportedListRecipientsByPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get imported list recipients by page
    ApiResponse<FetchImportedListRecipientsByPage200Response> response = apiInstance.FetchImportedListRecipientsByPageWithHttpInfo(listID, pageSize, pageNum, isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.FetchImportedListRecipientsByPageWithHttpInfo: " + e.Message);
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
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**FetchImportedListRecipientsByPage200Response**](FetchImportedListRecipientsByPage200Response.md)

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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all opt in list sources
                Object result = apiInstance.FetchOptInListSources(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.FetchOptInListSources: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.FetchOptInListSourcesWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.FetchOptInListSubscribers: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.FetchOptInListSubscribersWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.FetchOptInListSubscribersByPage: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.FetchOptInListSubscribersByPageWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get opt in lists
                List<OptInList> result = apiInstance.FetchOptInListsAssociatedWithPhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.FetchOptInListsAssociatedWithPhoneNumber: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.FetchOptInListsAssociatedWithPhoneNumberWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.FetchOptInSourceSubscribers: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.FetchOptInSourceSubscribersWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get opt in sources
                List<OptInListSource> result = apiInstance.FetchOptInSourcesAssociatedWithPhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.FetchOptInSourcesAssociatedWithPhoneNumber: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.FetchOptInSourcesAssociatedWithPhoneNumberWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.FetchOutboundSMS: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.FetchOutboundSMSWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.FetchOutboundSMSByPage: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.FetchOutboundSMSByPageWithHttpInfo: " + e.Message);
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

<a id="fetchpaymentobjectbroadcasts"></a>
# **FetchPaymentObjectBroadcasts**
> List&lt;StaticVoucherCampaignBroadcast&gt; FetchPaymentObjectBroadcasts (string phoneNumberID)

Get payment object broadcasts

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
    public class FetchPaymentObjectBroadcastsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get payment object broadcasts
                List<StaticVoucherCampaignBroadcast> result = apiInstance.FetchPaymentObjectBroadcasts(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.FetchPaymentObjectBroadcasts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchPaymentObjectBroadcastsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get payment object broadcasts
    ApiResponse<List<StaticVoucherCampaignBroadcast>> response = apiInstance.FetchPaymentObjectBroadcastsWithHttpInfo(phoneNumberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.FetchPaymentObjectBroadcastsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |

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

<a id="fetchsmsagreement"></a>
# **FetchSMSAgreement**
> Object FetchSMSAgreement ()

Get SMS Agreement

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
    public class FetchSMSAgreementExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);

            try
            {
                // Get SMS Agreement
                Object result = apiInstance.FetchSMSAgreement();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.FetchSMSAgreement: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchSMSAgreementWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get SMS Agreement
    ApiResponse<Object> response = apiInstance.FetchSMSAgreementWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.FetchSMSAgreementWithHttpInfo: " + e.Message);
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

<a id="importimportedlistrecipients"></a>
# **ImportImportedListRecipients**
> string ImportImportedListRecipients (string importedListID, WTEmployeeImportRecords wTEmployeeImportRecords)

Import imported list recipients

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
    public class ImportImportedListRecipientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var importedListID = "importedListID_example";  // string | 
            var wTEmployeeImportRecords = new WTEmployeeImportRecords(); // WTEmployeeImportRecords | 

            try
            {
                // Import imported list recipients
                string result = apiInstance.ImportImportedListRecipients(importedListID, wTEmployeeImportRecords);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.ImportImportedListRecipients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImportImportedListRecipientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Import imported list recipients
    ApiResponse<string> response = apiInstance.ImportImportedListRecipientsWithHttpInfo(importedListID, wTEmployeeImportRecords);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.ImportImportedListRecipientsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **importedListID** | **string** |  |  |
| **wTEmployeeImportRecords** | [**WTEmployeeImportRecords**](WTEmployeeImportRecords.md) |  |  |

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

<a id="importimportedlistrecipientsfrommembershiptier"></a>
# **ImportImportedListRecipientsFromMembershipTier**
> string ImportImportedListRecipientsFromMembershipTier (WTImportedListRecipientFromMembershipTierImport wTImportedListRecipientFromMembershipTierImport)

Import imported list recipients from a given membership tier

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
    public class ImportImportedListRecipientsFromMembershipTierExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var wTImportedListRecipientFromMembershipTierImport = new WTImportedListRecipientFromMembershipTierImport(); // WTImportedListRecipientFromMembershipTierImport | 

            try
            {
                // Import imported list recipients from a given membership tier
                string result = apiInstance.ImportImportedListRecipientsFromMembershipTier(wTImportedListRecipientFromMembershipTierImport);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.ImportImportedListRecipientsFromMembershipTier: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImportImportedListRecipientsFromMembershipTierWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Import imported list recipients from a given membership tier
    ApiResponse<string> response = apiInstance.ImportImportedListRecipientsFromMembershipTierWithHttpInfo(wTImportedListRecipientFromMembershipTierImport);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.ImportImportedListRecipientsFromMembershipTierWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTImportedListRecipientFromMembershipTierImport** | [**WTImportedListRecipientFromMembershipTierImport**](WTImportedListRecipientFromMembershipTierImport.md) |  |  |

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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.ImportOptInListSubscribers: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.ImportOptInListSubscribersWithHttpInfo: " + e.Message);
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

<a id="restorephonenumber"></a>
# **RestorePhoneNumber**
> PhoneNumber RestorePhoneNumber (string phoneNumberID)

Restore phone number

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
    public class RestorePhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Restore phone number
                PhoneNumber result = apiInstance.RestorePhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.RestorePhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestorePhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore phone number
    ApiResponse<PhoneNumber> response = apiInstance.RestorePhoneNumberWithHttpInfo(phoneNumberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.RestorePhoneNumberWithHttpInfo: " + e.Message);
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

<a id="restorerecipient"></a>
# **RestoreRecipient**
> ImportedListRecipient RestoreRecipient (string id)

Restore recipient

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
    public class RestoreRecipientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore recipient
                ImportedListRecipient result = apiInstance.RestoreRecipient(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.RestoreRecipient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreRecipientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore recipient
    ApiResponse<ImportedListRecipient> response = apiInstance.RestoreRecipientWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.RestoreRecipientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**ImportedListRecipient**](ImportedListRecipient.md)

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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);

            try
            {
                // Retrieve the number of messages sent by the merchant within the current billing cycle
                Object result = apiInstance.RetrieveSentAndMaxCountOfMessages();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.RetrieveSentAndMaxCountOfMessages: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.RetrieveSentAndMaxCountOfMessagesWithHttpInfo: " + e.Message);
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

<a id="saveimportedlist"></a>
# **SaveImportedList**
> ImportedList SaveImportedList (string listID, WTSMSImportedListCreate wTSMSImportedListCreate)

Save imported list

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
    public class SaveImportedListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var wTSMSImportedListCreate = new WTSMSImportedListCreate(); // WTSMSImportedListCreate | 

            try
            {
                // Save imported list
                ImportedList result = apiInstance.SaveImportedList(listID, wTSMSImportedListCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.SaveImportedList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveImportedListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Save imported list
    ApiResponse<ImportedList> response = apiInstance.SaveImportedListWithHttpInfo(listID, wTSMSImportedListCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.SaveImportedListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **wTSMSImportedListCreate** | [**WTSMSImportedListCreate**](WTSMSImportedListCreate.md) |  |  |

### Return type

[**ImportedList**](ImportedList.md)

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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.SaveOptInList: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.SaveOptInListWithHttpInfo: " + e.Message);
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
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling SMSOperationsApi.SaveOptInListSource: " + e.Message);
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
    Debug.Print("Exception when calling SMSOperationsApi.SaveOptInListSourceWithHttpInfo: " + e.Message);
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

<a id="sendphonenumberforverification"></a>
# **SendPhoneNumberForVerification**
> string SendPhoneNumberForVerification (string phoneNumberID, WTSMSUpdatePhoneNumberConfig wTSMSUpdatePhoneNumberConfig)

Request phone number verification

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
    public class SendPhoneNumberForVerificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var wTSMSUpdatePhoneNumberConfig = new WTSMSUpdatePhoneNumberConfig(); // WTSMSUpdatePhoneNumberConfig | 

            try
            {
                // Request phone number verification
                string result = apiInstance.SendPhoneNumberForVerification(phoneNumberID, wTSMSUpdatePhoneNumberConfig);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.SendPhoneNumberForVerification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendPhoneNumberForVerificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Request phone number verification
    ApiResponse<string> response = apiInstance.SendPhoneNumberForVerificationWithHttpInfo(phoneNumberID, wTSMSUpdatePhoneNumberConfig);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.SendPhoneNumberForVerificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **wTSMSUpdatePhoneNumberConfig** | [**WTSMSUpdatePhoneNumberConfig**](WTSMSUpdatePhoneNumberConfig.md) |  |  |

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

<a id="updatephonenumber"></a>
# **UpdatePhoneNumber**
> PhoneNumber UpdatePhoneNumber (string phoneNumberID, WTSMSUpdatePhoneNumberConfig wTSMSUpdatePhoneNumberConfig)

Update phone number

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
    public class UpdatePhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new SMSOperationsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 
            var wTSMSUpdatePhoneNumberConfig = new WTSMSUpdatePhoneNumberConfig(); // WTSMSUpdatePhoneNumberConfig | 

            try
            {
                // Update phone number
                PhoneNumber result = apiInstance.UpdatePhoneNumber(phoneNumberID, wTSMSUpdatePhoneNumberConfig);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SMSOperationsApi.UpdatePhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdatePhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update phone number
    ApiResponse<PhoneNumber> response = apiInstance.UpdatePhoneNumberWithHttpInfo(phoneNumberID, wTSMSUpdatePhoneNumberConfig);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SMSOperationsApi.UpdatePhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phoneNumberID** | **string** |  |  |
| **wTSMSUpdatePhoneNumberConfig** | [**WTSMSUpdatePhoneNumberConfig**](WTSMSUpdatePhoneNumberConfig.md) |  |  |

### Return type

[**PhoneNumber**](PhoneNumber.md)

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

