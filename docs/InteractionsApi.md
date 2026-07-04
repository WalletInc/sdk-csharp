# WalletInc.Api.InteractionsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ClaimTicket**](InteractionsApi.md#claimticket) | **PUT** /wallet/ticket/claim/{id} | Claim a ticket by ID |
| [**CreateAdvertisementCreditScan**](InteractionsApi.md#createadvertisementcreditscan) | **POST** /wallet/advertisementCredit/scan/{adCreditID} | Create ad credit scan |
| [**CreateEmployeeVCard**](InteractionsApi.md#createemployeevcard) | **GET** /wallet/employee/vcard/{id} | Download a representative&#39;s Virtual Business Card |
| [**CreateIcsFile**](InteractionsApi.md#createicsfile) | **GET** /wallet/liveevent/ics/{id} | Get ICS for live event |
| [**CreateVirtualBusinessCardVCard**](InteractionsApi.md#createvirtualbusinesscardvcard) | **GET** /wallet/virtualBusinessCard/vCard/{id} | Download a non-representative&#39;s Virtual Business Card |
| [**FetchActiveDynamicVouchers**](InteractionsApi.md#fetchactivedynamicvouchers) | **GET** /wallet/dyanmicVoucher/fetchActive | Get a merchant&#39;s active dynamic vouchers |
| [**FetchAdvertisementCreditScansFromList**](InteractionsApi.md#fetchadvertisementcreditscansfromlist) | **POST** /wallet/advertisementCredit/fetchScans/{merchantID} | Get multiple credit scans w/ array of IDs |
| [**FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID**](InteractionsApi.md#fetchallstaticvouchersassociatedwithcustomerwithvoucherid) | **GET** /wallet/staticVoucher/all | Get a customer&#39;s static vouchers on the basis of a given voucher ID |
| [**FetchCustomerTicketsWithToken**](InteractionsApi.md#fetchcustomerticketswithtoken) | **POST** /wallet/tickets/fetchCustomerTicketsWithToken | Get a customer&#39;s upcoming tickets via phone verification token |
| [**FetchDynamicVoucherWithVoucherID**](InteractionsApi.md#fetchdynamicvoucherwithvoucherid) | **GET** /wallet/dynamicVoucher/{voucherID} | Get dynamic voucher |
| [**FetchMemberInformation**](InteractionsApi.md#fetchmemberinformation) | **GET** /wallet/member | Get member information |
| [**FetchStaticVoucherWithVoucherID**](InteractionsApi.md#fetchstaticvoucherwithvoucherid) | **GET** /wallet/staticVoucher/{voucherID} | Get static voucher |
| [**FetchWalletPageWithToken**](InteractionsApi.md#fetchwalletpagewithtoken) | **POST** /wallet/page/token | Get page with token NOTE: This route exists because a token can completely change the dataset returned to the client. A simple fetch just logs the token with the request, but a fetchWithToken request can have a very different object returned to the client. |
| [**FetchWalletPaymentObjectsWithToken**](InteractionsApi.md#fetchwalletpaymentobjectswithtoken) | **POST** /wallet/paymentObject/token | Get payment objects with token NOTE: This route exists because a token can completely change the dataset returned to the client. A simple fetch just logs the token with the request, but a fetchWithToken request can have a very different object returned to the client. |
| [**FindByVanityHandle**](InteractionsApi.md#findbyvanityhandle) | **GET** /wallet/vanityHandle/{handle} | Get vanity handle |
| [**IdentifyItem**](InteractionsApi.md#identifyitem) | **GET** /wallet/item/identify/{itemID} | Identify item |
| [**RequestMerchantURLRedirect**](InteractionsApi.md#requestmerchanturlredirect) | **POST** /wallet/merchantURL/{itemID} | Request Merchant URL |
| [**SubscribeEmail**](InteractionsApi.md#subscribeemail) | **POST** /wallet/subscribeEmail | Create email subscriber |
| [**SubscribeSms**](InteractionsApi.md#subscribesms) | **POST** /wallet/subscribeSms | Create sms subscriber |

<a id="claimticket"></a>
# **ClaimTicket**
> Ticket ClaimTicket (string id, ClaimTicketRequest claimTicketRequest)

Claim a ticket by ID

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
    public class ClaimTicketExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 
            var claimTicketRequest = new ClaimTicketRequest(); // ClaimTicketRequest | 

            try
            {
                // Claim a ticket by ID
                Ticket result = apiInstance.ClaimTicket(id, claimTicketRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.ClaimTicket: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ClaimTicketWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Claim a ticket by ID
    ApiResponse<Ticket> response = apiInstance.ClaimTicketWithHttpInfo(id, claimTicketRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.ClaimTicketWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |
| **claimTicketRequest** | [**ClaimTicketRequest**](ClaimTicketRequest.md) |  |  |

### Return type

[**Ticket**](Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createadvertisementcreditscan"></a>
# **CreateAdvertisementCreditScan**
> AdvertisementCreditScan CreateAdvertisementCreditScan (string adCreditID)

Create ad credit scan

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
    public class CreateAdvertisementCreditScanExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var adCreditID = "adCreditID_example";  // string | 

            try
            {
                // Create ad credit scan
                AdvertisementCreditScan result = apiInstance.CreateAdvertisementCreditScan(adCreditID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.CreateAdvertisementCreditScan: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAdvertisementCreditScanWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create ad credit scan
    ApiResponse<AdvertisementCreditScan> response = apiInstance.CreateAdvertisementCreditScanWithHttpInfo(adCreditID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.CreateAdvertisementCreditScanWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adCreditID** | **string** |  |  |

### Return type

[**AdvertisementCreditScan**](AdvertisementCreditScan.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createemployeevcard"></a>
# **CreateEmployeeVCard**
> string CreateEmployeeVCard (string id)

Download a representative's Virtual Business Card

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
    public class CreateEmployeeVCardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Download a representative's Virtual Business Card
                string result = apiInstance.CreateEmployeeVCard(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.CreateEmployeeVCard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEmployeeVCardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download a representative's Virtual Business Card
    ApiResponse<string> response = apiInstance.CreateEmployeeVCardWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.CreateEmployeeVCardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createicsfile"></a>
# **CreateIcsFile**
> Object CreateIcsFile (string id)

Get ICS for live event

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
    public class CreateIcsFileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get ICS for live event
                Object result = apiInstance.CreateIcsFile(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.CreateIcsFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateIcsFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ICS for live event
    ApiResponse<Object> response = apiInstance.CreateIcsFileWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.CreateIcsFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="createvirtualbusinesscardvcard"></a>
# **CreateVirtualBusinessCardVCard**
> string CreateVirtualBusinessCardVCard (string id)

Download a non-representative's Virtual Business Card

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
    public class CreateVirtualBusinessCardVCardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Download a non-representative's Virtual Business Card
                string result = apiInstance.CreateVirtualBusinessCardVCard(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.CreateVirtualBusinessCardVCard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateVirtualBusinessCardVCardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download a non-representative's Virtual Business Card
    ApiResponse<string> response = apiInstance.CreateVirtualBusinessCardVCardWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.CreateVirtualBusinessCardVCardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchactivedynamicvouchers"></a>
# **FetchActiveDynamicVouchers**
> List&lt;DynamicVoucher&gt; FetchActiveDynamicVouchers (string merchantID)

Get a merchant's active dynamic vouchers

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
    public class FetchActiveDynamicVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var merchantID = "merchantID_example";  // string | 

            try
            {
                // Get a merchant's active dynamic vouchers
                List<DynamicVoucher> result = apiInstance.FetchActiveDynamicVouchers(merchantID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchActiveDynamicVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchActiveDynamicVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a merchant's active dynamic vouchers
    ApiResponse<List<DynamicVoucher>> response = apiInstance.FetchActiveDynamicVouchersWithHttpInfo(merchantID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchActiveDynamicVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **merchantID** | **string** |  |  |

### Return type

[**List&lt;DynamicVoucher&gt;**](DynamicVoucher.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchadvertisementcreditscansfromlist"></a>
# **FetchAdvertisementCreditScansFromList**
> List&lt;Object&gt; FetchAdvertisementCreditScansFromList (string merchantID, FetchAdvertisementCreditScansFromListRequest fetchAdvertisementCreditScansFromListRequest)

Get multiple credit scans w/ array of IDs

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
    public class FetchAdvertisementCreditScansFromListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var merchantID = "merchantID_example";  // string | 
            var fetchAdvertisementCreditScansFromListRequest = new FetchAdvertisementCreditScansFromListRequest(); // FetchAdvertisementCreditScansFromListRequest | 

            try
            {
                // Get multiple credit scans w/ array of IDs
                List<Object> result = apiInstance.FetchAdvertisementCreditScansFromList(merchantID, fetchAdvertisementCreditScansFromListRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchAdvertisementCreditScansFromList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAdvertisementCreditScansFromListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get multiple credit scans w/ array of IDs
    ApiResponse<List<Object>> response = apiInstance.FetchAdvertisementCreditScansFromListWithHttpInfo(merchantID, fetchAdvertisementCreditScansFromListRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchAdvertisementCreditScansFromListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **merchantID** | **string** |  |  |
| **fetchAdvertisementCreditScansFromListRequest** | [**FetchAdvertisementCreditScansFromListRequest**](FetchAdvertisementCreditScansFromListRequest.md) |  |  |

### Return type

**List<Object>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchallstaticvouchersassociatedwithcustomerwithvoucherid"></a>
# **FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID**
> List&lt;FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID200ResponseInner&gt; FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID (string voucherID)

Get a customer's static vouchers on the basis of a given voucher ID

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
    public class FetchAllStaticVouchersAssociatedWithCustomerWithVoucherIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var voucherID = "voucherID_example";  // string | 

            try
            {
                // Get a customer's static vouchers on the basis of a given voucher ID
                List<FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID200ResponseInner> result = apiInstance.FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID(voucherID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllStaticVouchersAssociatedWithCustomerWithVoucherIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a customer's static vouchers on the basis of a given voucher ID
    ApiResponse<List<FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID200ResponseInner>> response = apiInstance.FetchAllStaticVouchersAssociatedWithCustomerWithVoucherIDWithHttpInfo(voucherID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchAllStaticVouchersAssociatedWithCustomerWithVoucherIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **voucherID** | **string** |  |  |

### Return type

[**List&lt;FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID200ResponseInner&gt;**](FetchAllStaticVouchersAssociatedWithCustomerWithVoucherID200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchcustomerticketswithtoken"></a>
# **FetchCustomerTicketsWithToken**
> List&lt;Ticket&gt; FetchCustomerTicketsWithToken (FetchCustomerTicketsWithTokenRequest fetchCustomerTicketsWithTokenRequest)

Get a customer's upcoming tickets via phone verification token

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
    public class FetchCustomerTicketsWithTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var fetchCustomerTicketsWithTokenRequest = new FetchCustomerTicketsWithTokenRequest(); // FetchCustomerTicketsWithTokenRequest | 

            try
            {
                // Get a customer's upcoming tickets via phone verification token
                List<Ticket> result = apiInstance.FetchCustomerTicketsWithToken(fetchCustomerTicketsWithTokenRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchCustomerTicketsWithToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchCustomerTicketsWithTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a customer's upcoming tickets via phone verification token
    ApiResponse<List<Ticket>> response = apiInstance.FetchCustomerTicketsWithTokenWithHttpInfo(fetchCustomerTicketsWithTokenRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchCustomerTicketsWithTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fetchCustomerTicketsWithTokenRequest** | [**FetchCustomerTicketsWithTokenRequest**](FetchCustomerTicketsWithTokenRequest.md) |  |  |

### Return type

[**List&lt;Ticket&gt;**](Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchdynamicvoucherwithvoucherid"></a>
# **FetchDynamicVoucherWithVoucherID**
> DynamicVoucher FetchDynamicVoucherWithVoucherID (string voucherID)

Get dynamic voucher

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
    public class FetchDynamicVoucherWithVoucherIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var voucherID = "voucherID_example";  // string | 

            try
            {
                // Get dynamic voucher
                DynamicVoucher result = apiInstance.FetchDynamicVoucherWithVoucherID(voucherID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchDynamicVoucherWithVoucherID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDynamicVoucherWithVoucherIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get dynamic voucher
    ApiResponse<DynamicVoucher> response = apiInstance.FetchDynamicVoucherWithVoucherIDWithHttpInfo(voucherID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchDynamicVoucherWithVoucherIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **voucherID** | **string** |  |  |

### Return type

[**DynamicVoucher**](DynamicVoucher.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchmemberinformation"></a>
# **FetchMemberInformation**
> Member FetchMemberInformation (string memberID, string merchantID)

Get member information

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
    public class FetchMemberInformationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var memberID = "memberID_example";  // string | 
            var merchantID = "merchantID_example";  // string | 

            try
            {
                // Get member information
                Member result = apiInstance.FetchMemberInformation(memberID, merchantID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchMemberInformation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMemberInformationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get member information
    ApiResponse<Member> response = apiInstance.FetchMemberInformationWithHttpInfo(memberID, merchantID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchMemberInformationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **memberID** | **string** |  |  |
| **merchantID** | **string** |  |  |

### Return type

[**Member**](Member.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchstaticvoucherwithvoucherid"></a>
# **FetchStaticVoucherWithVoucherID**
> StaticVoucher FetchStaticVoucherWithVoucherID (string voucherID)

Get static voucher

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
    public class FetchStaticVoucherWithVoucherIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var voucherID = "voucherID_example";  // string | 

            try
            {
                // Get static voucher
                StaticVoucher result = apiInstance.FetchStaticVoucherWithVoucherID(voucherID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchStaticVoucherWithVoucherID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchStaticVoucherWithVoucherIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get static voucher
    ApiResponse<StaticVoucher> response = apiInstance.FetchStaticVoucherWithVoucherIDWithHttpInfo(voucherID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchStaticVoucherWithVoucherIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **voucherID** | **string** |  |  |

### Return type

[**StaticVoucher**](StaticVoucher.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchwalletpagewithtoken"></a>
# **FetchWalletPageWithToken**
> Object FetchWalletPageWithToken (WTFetchWalletPaymentObjectsWithToken wTFetchWalletPaymentObjectsWithToken)

Get page with token NOTE: This route exists because a token can completely change the dataset returned to the client. A simple fetch just logs the token with the request, but a fetchWithToken request can have a very different object returned to the client.

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
    public class FetchWalletPageWithTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var wTFetchWalletPaymentObjectsWithToken = new WTFetchWalletPaymentObjectsWithToken(); // WTFetchWalletPaymentObjectsWithToken | 

            try
            {
                // Get page with token NOTE: This route exists because a token can completely change the dataset returned to the client. A simple fetch just logs the token with the request, but a fetchWithToken request can have a very different object returned to the client.
                Object result = apiInstance.FetchWalletPageWithToken(wTFetchWalletPaymentObjectsWithToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchWalletPageWithToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletPageWithTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get page with token NOTE: This route exists because a token can completely change the dataset returned to the client. A simple fetch just logs the token with the request, but a fetchWithToken request can have a very different object returned to the client.
    ApiResponse<Object> response = apiInstance.FetchWalletPageWithTokenWithHttpInfo(wTFetchWalletPaymentObjectsWithToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchWalletPageWithTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTFetchWalletPaymentObjectsWithToken** | [**WTFetchWalletPaymentObjectsWithToken**](WTFetchWalletPaymentObjectsWithToken.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetchwalletpaymentobjectswithtoken"></a>
# **FetchWalletPaymentObjectsWithToken**
> Object FetchWalletPaymentObjectsWithToken (WTFetchWalletPaymentObjectsWithToken wTFetchWalletPaymentObjectsWithToken)

Get payment objects with token NOTE: This route exists because a token can completely change the dataset returned to the client. A simple fetch just logs the token with the request, but a fetchWithToken request can have a very different object returned to the client.

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
    public class FetchWalletPaymentObjectsWithTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var wTFetchWalletPaymentObjectsWithToken = new WTFetchWalletPaymentObjectsWithToken(); // WTFetchWalletPaymentObjectsWithToken | 

            try
            {
                // Get payment objects with token NOTE: This route exists because a token can completely change the dataset returned to the client. A simple fetch just logs the token with the request, but a fetchWithToken request can have a very different object returned to the client.
                Object result = apiInstance.FetchWalletPaymentObjectsWithToken(wTFetchWalletPaymentObjectsWithToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FetchWalletPaymentObjectsWithToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletPaymentObjectsWithTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get payment objects with token NOTE: This route exists because a token can completely change the dataset returned to the client. A simple fetch just logs the token with the request, but a fetchWithToken request can have a very different object returned to the client.
    ApiResponse<Object> response = apiInstance.FetchWalletPaymentObjectsWithTokenWithHttpInfo(wTFetchWalletPaymentObjectsWithToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FetchWalletPaymentObjectsWithTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTFetchWalletPaymentObjectsWithToken** | [**WTFetchWalletPaymentObjectsWithToken**](WTFetchWalletPaymentObjectsWithToken.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="findbyvanityhandle"></a>
# **FindByVanityHandle**
> WalletConfiguration FindByVanityHandle (string handle)

Get vanity handle

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
    public class FindByVanityHandleExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var handle = "handle_example";  // string | 

            try
            {
                // Get vanity handle
                WalletConfiguration result = apiInstance.FindByVanityHandle(handle);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.FindByVanityHandle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FindByVanityHandleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get vanity handle
    ApiResponse<WalletConfiguration> response = apiInstance.FindByVanityHandleWithHttpInfo(handle);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.FindByVanityHandleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **handle** | **string** |  |  |

### Return type

[**WalletConfiguration**](WalletConfiguration.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="identifyitem"></a>
# **IdentifyItem**
> Object IdentifyItem (string itemID, bool? isRefresh = null, string? phoneVerificationToken = null, string? referrer = null)

Identify item

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
    public class IdentifyItemExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 
            var isRefresh = true;  // bool? |  (optional) 
            var phoneVerificationToken = "phoneVerificationToken_example";  // string? |  (optional) 
            var referrer = "referrer_example";  // string? |  (optional) 

            try
            {
                // Identify item
                Object result = apiInstance.IdentifyItem(itemID, isRefresh, phoneVerificationToken, referrer);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.IdentifyItem: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdentifyItemWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Identify item
    ApiResponse<Object> response = apiInstance.IdentifyItemWithHttpInfo(itemID, isRefresh, phoneVerificationToken, referrer);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.IdentifyItemWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemID** | **string** |  |  |
| **isRefresh** | **bool?** |  | [optional]  |
| **phoneVerificationToken** | **string?** |  | [optional]  |
| **referrer** | **string?** |  | [optional]  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="requestmerchanturlredirect"></a>
# **RequestMerchantURLRedirect**
> Object RequestMerchantURLRedirect (string itemID, BrowserDetails browserDetails)

Request Merchant URL

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
    public class RequestMerchantURLRedirectExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 
            var browserDetails = new BrowserDetails(); // BrowserDetails | 

            try
            {
                // Request Merchant URL
                Object result = apiInstance.RequestMerchantURLRedirect(itemID, browserDetails);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.RequestMerchantURLRedirect: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestMerchantURLRedirectWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Request Merchant URL
    ApiResponse<Object> response = apiInstance.RequestMerchantURLRedirectWithHttpInfo(itemID, browserDetails);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.RequestMerchantURLRedirectWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemID** | **string** |  |  |
| **browserDetails** | [**BrowserDetails**](BrowserDetails.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscribeemail"></a>
# **SubscribeEmail**
> EmailSubscriber SubscribeEmail (WTEmailSubscriberCreateParamsWalletUI wTEmailSubscriberCreateParamsWalletUI)

Create email subscriber

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
    public class SubscribeEmailExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var wTEmailSubscriberCreateParamsWalletUI = new WTEmailSubscriberCreateParamsWalletUI(); // WTEmailSubscriberCreateParamsWalletUI | 

            try
            {
                // Create email subscriber
                EmailSubscriber result = apiInstance.SubscribeEmail(wTEmailSubscriberCreateParamsWalletUI);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.SubscribeEmail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscribeEmailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create email subscriber
    ApiResponse<EmailSubscriber> response = apiInstance.SubscribeEmailWithHttpInfo(wTEmailSubscriberCreateParamsWalletUI);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.SubscribeEmailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmailSubscriberCreateParamsWalletUI** | [**WTEmailSubscriberCreateParamsWalletUI**](WTEmailSubscriberCreateParamsWalletUI.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscribesms"></a>
# **SubscribeSms**
> SmsSubscriber SubscribeSms (WTSmsSubscriberCreateParamsWalletUI wTSmsSubscriberCreateParamsWalletUI)

Create sms subscriber

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
    public class SubscribeSmsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InteractionsApi(httpClient, config, httpClientHandler);
            var wTSmsSubscriberCreateParamsWalletUI = new WTSmsSubscriberCreateParamsWalletUI(); // WTSmsSubscriberCreateParamsWalletUI | 

            try
            {
                // Create sms subscriber
                SmsSubscriber result = apiInstance.SubscribeSms(wTSmsSubscriberCreateParamsWalletUI);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InteractionsApi.SubscribeSms: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscribeSmsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create sms subscriber
    ApiResponse<SmsSubscriber> response = apiInstance.SubscribeSmsWithHttpInfo(wTSmsSubscriberCreateParamsWalletUI);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InteractionsApi.SubscribeSmsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTSmsSubscriberCreateParamsWalletUI** | [**WTSmsSubscriberCreateParamsWalletUI**](WTSmsSubscriberCreateParamsWalletUI.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

