# WalletInc.Api.BroadcastsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchivePaymentObjectBroadcast**](BroadcastsApi.md#archivepaymentobjectbroadcast) | **DELETE** /v2/merchant/paymentObjectBroadcast/{broadcastID} | Archive payment object broadcast |
| [**FetchAdvertisementCreditBroadcasts**](BroadcastsApi.md#fetchadvertisementcreditbroadcasts) | **GET** /v2/merchant/broadcasts/adCredits/all | Get all ad credit broadcasts |
| [**FetchDynamicVoucherBroadcasts**](BroadcastsApi.md#fetchdynamicvoucherbroadcasts) | **GET** /v2/merchant/broadcasts/dynamicVouchers/all | Get all dynamic voucher broadcasts |
| [**FetchPaymentObjectBroadcasts**](BroadcastsApi.md#fetchpaymentobjectbroadcasts) | **GET** /v2/sms/paymentObjectBroadcasts/{phoneNumberID} | Get payment object broadcasts |
| [**FetchSimpleSMSBroadcasts**](BroadcastsApi.md#fetchsimplesmsbroadcasts) | **GET** /v2/merchant/broadcasts/simpleSMS/all | Get all simple SMS broadcasts |
| [**FetchStaticVoucherCampaignBroadcasts**](BroadcastsApi.md#fetchstaticvouchercampaignbroadcasts) | **GET** /v2/merchant/broadcasts/staticVoucherCampaign/all | Get all static voucher campaign broadcasts |
| [**ScheduleAdvertisementCredit**](BroadcastsApi.md#scheduleadvertisementcredit) | **POST** /v2/employee/sms/schedule/adCredit/{advertisementCreditID} | Schedule Ad Credit |
| [**ScheduleDynamicVoucher**](BroadcastsApi.md#scheduledynamicvoucher) | **POST** /v2/employee/sms/schedule/dynamicVoucher/{dynamicVoucherID} | Schedule Dynamic Voucher to list |
| [**ScheduleDynamicVoucherToRecipient**](BroadcastsApi.md#scheduledynamicvouchertorecipient) | **POST** /v2/employee/sms/schedule/recipient/dynamicVoucher/{dynamicVoucherID} | Schedule Dynamic Voucher to recipient |
| [**ScheduleSimpleSMS**](BroadcastsApi.md#schedulesimplesms) | **POST** /v2/employee/sms/schedule/simple | Schedule Simple SMS broadcast to list |
| [**ScheduleSimpleSMSToRecipient**](BroadcastsApi.md#schedulesimplesmstorecipient) | **POST** /v2/employee/sms/schedule/recipient/simple | Schedule Simple SMS broadcast to recipient |
| [**SendSmsCampaignBroadcast**](BroadcastsApi.md#sendsmscampaignbroadcast) | **POST** /v2/employee/sms/schedule/campaign/{staticVoucherCampaignID} | Schedule SMS Campaign Broadcast |

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
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var broadcastID = "broadcastID_example";  // string | 

            try
            {
                // Archive payment object broadcast
                Object result = apiInstance.ArchivePaymentObjectBroadcast(broadcastID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.ArchivePaymentObjectBroadcast: " + e.Message);
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
    Debug.Print("Exception when calling BroadcastsApi.ArchivePaymentObjectBroadcastWithHttpInfo: " + e.Message);
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
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all ad credit broadcasts
                List<AdvertisementCreditBroadcast> result = apiInstance.FetchAdvertisementCreditBroadcasts(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.FetchAdvertisementCreditBroadcasts: " + e.Message);
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
    Debug.Print("Exception when calling BroadcastsApi.FetchAdvertisementCreditBroadcastsWithHttpInfo: " + e.Message);
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
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all dynamic voucher broadcasts
                List<DynamicVoucherBroadcast> result = apiInstance.FetchDynamicVoucherBroadcasts(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.FetchDynamicVoucherBroadcasts: " + e.Message);
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
    Debug.Print("Exception when calling BroadcastsApi.FetchDynamicVoucherBroadcastsWithHttpInfo: " + e.Message);
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
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get payment object broadcasts
                List<StaticVoucherCampaignBroadcast> result = apiInstance.FetchPaymentObjectBroadcasts(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.FetchPaymentObjectBroadcasts: " + e.Message);
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
    Debug.Print("Exception when calling BroadcastsApi.FetchPaymentObjectBroadcastsWithHttpInfo: " + e.Message);
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
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all simple SMS broadcasts
                List<SimpleSMSBroadcast> result = apiInstance.FetchSimpleSMSBroadcasts(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.FetchSimpleSMSBroadcasts: " + e.Message);
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
    Debug.Print("Exception when calling BroadcastsApi.FetchSimpleSMSBroadcastsWithHttpInfo: " + e.Message);
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
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all static voucher campaign broadcasts
                List<StaticVoucherCampaignBroadcast> result = apiInstance.FetchStaticVoucherCampaignBroadcasts(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.FetchStaticVoucherCampaignBroadcasts: " + e.Message);
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
    Debug.Print("Exception when calling BroadcastsApi.FetchStaticVoucherCampaignBroadcastsWithHttpInfo: " + e.Message);
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

<a id="scheduleadvertisementcredit"></a>
# **ScheduleAdvertisementCredit**
> AdvertisementCreditBroadcast ScheduleAdvertisementCredit (string advertisementCreditID, WTEmployeeScheduleSimpleSMS wTEmployeeScheduleSimpleSMS)

Schedule Ad Credit

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
    public class ScheduleAdvertisementCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var advertisementCreditID = "advertisementCreditID_example";  // string | 
            var wTEmployeeScheduleSimpleSMS = new WTEmployeeScheduleSimpleSMS(); // WTEmployeeScheduleSimpleSMS | 

            try
            {
                // Schedule Ad Credit
                AdvertisementCreditBroadcast result = apiInstance.ScheduleAdvertisementCredit(advertisementCreditID, wTEmployeeScheduleSimpleSMS);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.ScheduleAdvertisementCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleAdvertisementCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Ad Credit
    ApiResponse<AdvertisementCreditBroadcast> response = apiInstance.ScheduleAdvertisementCreditWithHttpInfo(advertisementCreditID, wTEmployeeScheduleSimpleSMS);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BroadcastsApi.ScheduleAdvertisementCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **advertisementCreditID** | **string** |  |  |
| **wTEmployeeScheduleSimpleSMS** | [**WTEmployeeScheduleSimpleSMS**](WTEmployeeScheduleSimpleSMS.md) |  |  |

### Return type

[**AdvertisementCreditBroadcast**](AdvertisementCreditBroadcast.md)

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

<a id="scheduledynamicvoucher"></a>
# **ScheduleDynamicVoucher**
> DynamicVoucherBroadcast ScheduleDynamicVoucher (string dynamicVoucherID, WTEmployeeScheduleSimpleSMS wTEmployeeScheduleSimpleSMS)

Schedule Dynamic Voucher to list

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
    public class ScheduleDynamicVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var dynamicVoucherID = "dynamicVoucherID_example";  // string | 
            var wTEmployeeScheduleSimpleSMS = new WTEmployeeScheduleSimpleSMS(); // WTEmployeeScheduleSimpleSMS | 

            try
            {
                // Schedule Dynamic Voucher to list
                DynamicVoucherBroadcast result = apiInstance.ScheduleDynamicVoucher(dynamicVoucherID, wTEmployeeScheduleSimpleSMS);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.ScheduleDynamicVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleDynamicVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Dynamic Voucher to list
    ApiResponse<DynamicVoucherBroadcast> response = apiInstance.ScheduleDynamicVoucherWithHttpInfo(dynamicVoucherID, wTEmployeeScheduleSimpleSMS);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BroadcastsApi.ScheduleDynamicVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dynamicVoucherID** | **string** |  |  |
| **wTEmployeeScheduleSimpleSMS** | [**WTEmployeeScheduleSimpleSMS**](WTEmployeeScheduleSimpleSMS.md) |  |  |

### Return type

[**DynamicVoucherBroadcast**](DynamicVoucherBroadcast.md)

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

<a id="scheduledynamicvouchertorecipient"></a>
# **ScheduleDynamicVoucherToRecipient**
> DynamicVoucherBroadcast ScheduleDynamicVoucherToRecipient (string dynamicVoucherID, WTEmployeeScheduleSimpleSMSToRecipient wTEmployeeScheduleSimpleSMSToRecipient)

Schedule Dynamic Voucher to recipient

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
    public class ScheduleDynamicVoucherToRecipientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var dynamicVoucherID = "dynamicVoucherID_example";  // string | 
            var wTEmployeeScheduleSimpleSMSToRecipient = new WTEmployeeScheduleSimpleSMSToRecipient(); // WTEmployeeScheduleSimpleSMSToRecipient | 

            try
            {
                // Schedule Dynamic Voucher to recipient
                DynamicVoucherBroadcast result = apiInstance.ScheduleDynamicVoucherToRecipient(dynamicVoucherID, wTEmployeeScheduleSimpleSMSToRecipient);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.ScheduleDynamicVoucherToRecipient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleDynamicVoucherToRecipientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Dynamic Voucher to recipient
    ApiResponse<DynamicVoucherBroadcast> response = apiInstance.ScheduleDynamicVoucherToRecipientWithHttpInfo(dynamicVoucherID, wTEmployeeScheduleSimpleSMSToRecipient);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BroadcastsApi.ScheduleDynamicVoucherToRecipientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dynamicVoucherID** | **string** |  |  |
| **wTEmployeeScheduleSimpleSMSToRecipient** | [**WTEmployeeScheduleSimpleSMSToRecipient**](WTEmployeeScheduleSimpleSMSToRecipient.md) |  |  |

### Return type

[**DynamicVoucherBroadcast**](DynamicVoucherBroadcast.md)

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

<a id="schedulesimplesms"></a>
# **ScheduleSimpleSMS**
> bool ScheduleSimpleSMS (WTEmployeeScheduleSimpleSMS wTEmployeeScheduleSimpleSMS)

Schedule Simple SMS broadcast to list

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
    public class ScheduleSimpleSMSExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var wTEmployeeScheduleSimpleSMS = new WTEmployeeScheduleSimpleSMS(); // WTEmployeeScheduleSimpleSMS | 

            try
            {
                // Schedule Simple SMS broadcast to list
                bool result = apiInstance.ScheduleSimpleSMS(wTEmployeeScheduleSimpleSMS);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.ScheduleSimpleSMS: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleSimpleSMSWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Simple SMS broadcast to list
    ApiResponse<bool> response = apiInstance.ScheduleSimpleSMSWithHttpInfo(wTEmployeeScheduleSimpleSMS);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BroadcastsApi.ScheduleSimpleSMSWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeScheduleSimpleSMS** | [**WTEmployeeScheduleSimpleSMS**](WTEmployeeScheduleSimpleSMS.md) |  |  |

### Return type

**bool**

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

<a id="schedulesimplesmstorecipient"></a>
# **ScheduleSimpleSMSToRecipient**
> bool ScheduleSimpleSMSToRecipient (WTEmployeeScheduleSimpleSMSToRecipient wTEmployeeScheduleSimpleSMSToRecipient)

Schedule Simple SMS broadcast to recipient

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
    public class ScheduleSimpleSMSToRecipientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var wTEmployeeScheduleSimpleSMSToRecipient = new WTEmployeeScheduleSimpleSMSToRecipient(); // WTEmployeeScheduleSimpleSMSToRecipient | 

            try
            {
                // Schedule Simple SMS broadcast to recipient
                bool result = apiInstance.ScheduleSimpleSMSToRecipient(wTEmployeeScheduleSimpleSMSToRecipient);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.ScheduleSimpleSMSToRecipient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleSimpleSMSToRecipientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Simple SMS broadcast to recipient
    ApiResponse<bool> response = apiInstance.ScheduleSimpleSMSToRecipientWithHttpInfo(wTEmployeeScheduleSimpleSMSToRecipient);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BroadcastsApi.ScheduleSimpleSMSToRecipientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeScheduleSimpleSMSToRecipient** | [**WTEmployeeScheduleSimpleSMSToRecipient**](WTEmployeeScheduleSimpleSMSToRecipient.md) |  |  |

### Return type

**bool**

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

<a id="sendsmscampaignbroadcast"></a>
# **SendSmsCampaignBroadcast**
> StaticVoucherCampaignBroadcast SendSmsCampaignBroadcast (string staticVoucherCampaignID, WTEmployeeScheduleSMSCampaignBroadcast wTEmployeeScheduleSMSCampaignBroadcast)

Schedule SMS Campaign Broadcast

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
    public class SendSmsCampaignBroadcastExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BroadcastsApi(httpClient, config, httpClientHandler);
            var staticVoucherCampaignID = "staticVoucherCampaignID_example";  // string | 
            var wTEmployeeScheduleSMSCampaignBroadcast = new WTEmployeeScheduleSMSCampaignBroadcast(); // WTEmployeeScheduleSMSCampaignBroadcast | 

            try
            {
                // Schedule SMS Campaign Broadcast
                StaticVoucherCampaignBroadcast result = apiInstance.SendSmsCampaignBroadcast(staticVoucherCampaignID, wTEmployeeScheduleSMSCampaignBroadcast);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BroadcastsApi.SendSmsCampaignBroadcast: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendSmsCampaignBroadcastWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule SMS Campaign Broadcast
    ApiResponse<StaticVoucherCampaignBroadcast> response = apiInstance.SendSmsCampaignBroadcastWithHttpInfo(staticVoucherCampaignID, wTEmployeeScheduleSMSCampaignBroadcast);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BroadcastsApi.SendSmsCampaignBroadcastWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **staticVoucherCampaignID** | **string** |  |  |
| **wTEmployeeScheduleSMSCampaignBroadcast** | [**WTEmployeeScheduleSMSCampaignBroadcast**](WTEmployeeScheduleSMSCampaignBroadcast.md) |  |  |

### Return type

[**StaticVoucherCampaignBroadcast**](StaticVoucherCampaignBroadcast.md)

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

