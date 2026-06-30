# WalletInc.Api.CustomerApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchActiveVouchers**](CustomerApi.md#fetchactivevouchers) | **GET** /v2/customer/vouchers/active | Get active static vouchers |
| [**FetchAllVouchers**](CustomerApi.md#fetchallvouchers) | **GET** /v2/customer/vouchers/all | Get all static vouchers |
| [**FetchExpiredVouchers**](CustomerApi.md#fetchexpiredvouchers) | **GET** /v2/customer/vouchers/expired | Get expired static vouchers |
| [**FetchRedeemedVouchers**](CustomerApi.md#fetchredeemedvouchers) | **GET** /v2/customer/vouchers/redeemed | Get redeemed static vouchers |
| [**FetchRefundedVouchers**](CustomerApi.md#fetchrefundedvouchers) | **GET** /v2/customer/vouchers/refunded | Get refunded static vouchers |
| [**FetchUpcomingVouchers**](CustomerApi.md#fetchupcomingvouchers) | **GET** /v2/customer/vouchers/upcoming | Get upcoming static vouchers |
| [**FetchWalletViewsForSession**](CustomerApi.md#fetchwalletviewsforsession) | **GET** /v2/customer/walletViews/session/{id} | Get Wallet Views for Session |
| [**SearchByMemberID**](CustomerApi.md#searchbymemberid) | **POST** /v2/customer/search/memberID | Find members with memberID |
| [**SearchByPhoneNumber**](CustomerApi.md#searchbyphonenumber) | **POST** /v2/customer/search/phoneNumber | Find members with phone number |

<a id="fetchactivevouchers"></a>
# **FetchActiveVouchers**
> List&lt;StaticVoucher&gt; FetchActiveVouchers (string? memberID = null, string? cellPhoneNumber = null)

Get active static vouchers

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
    public class FetchActiveVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var memberID = "memberID_example";  // string? |  (optional) 
            var cellPhoneNumber = "cellPhoneNumber_example";  // string? |  (optional) 

            try
            {
                // Get active static vouchers
                List<StaticVoucher> result = apiInstance.FetchActiveVouchers(memberID, cellPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.FetchActiveVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchActiveVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get active static vouchers
    ApiResponse<List<StaticVoucher>> response = apiInstance.FetchActiveVouchersWithHttpInfo(memberID, cellPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.FetchActiveVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **memberID** | **string?** |  | [optional]  |
| **cellPhoneNumber** | **string?** |  | [optional]  |

### Return type

[**List&lt;StaticVoucher&gt;**](StaticVoucher.md)

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

<a id="fetchallvouchers"></a>
# **FetchAllVouchers**
> List&lt;StaticVoucher&gt; FetchAllVouchers (string? memberID = null, string? cellPhoneNumber = null)

Get all static vouchers

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
    public class FetchAllVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var memberID = "memberID_example";  // string? |  (optional) 
            var cellPhoneNumber = "cellPhoneNumber_example";  // string? |  (optional) 

            try
            {
                // Get all static vouchers
                List<StaticVoucher> result = apiInstance.FetchAllVouchers(memberID, cellPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.FetchAllVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all static vouchers
    ApiResponse<List<StaticVoucher>> response = apiInstance.FetchAllVouchersWithHttpInfo(memberID, cellPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.FetchAllVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **memberID** | **string?** |  | [optional]  |
| **cellPhoneNumber** | **string?** |  | [optional]  |

### Return type

[**List&lt;StaticVoucher&gt;**](StaticVoucher.md)

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

<a id="fetchexpiredvouchers"></a>
# **FetchExpiredVouchers**
> List&lt;StaticVoucher&gt; FetchExpiredVouchers (string? memberID = null, string? cellPhoneNumber = null)

Get expired static vouchers

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
    public class FetchExpiredVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var memberID = "memberID_example";  // string? |  (optional) 
            var cellPhoneNumber = "cellPhoneNumber_example";  // string? |  (optional) 

            try
            {
                // Get expired static vouchers
                List<StaticVoucher> result = apiInstance.FetchExpiredVouchers(memberID, cellPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.FetchExpiredVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchExpiredVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get expired static vouchers
    ApiResponse<List<StaticVoucher>> response = apiInstance.FetchExpiredVouchersWithHttpInfo(memberID, cellPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.FetchExpiredVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **memberID** | **string?** |  | [optional]  |
| **cellPhoneNumber** | **string?** |  | [optional]  |

### Return type

[**List&lt;StaticVoucher&gt;**](StaticVoucher.md)

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

<a id="fetchredeemedvouchers"></a>
# **FetchRedeemedVouchers**
> List&lt;StaticVoucher&gt; FetchRedeemedVouchers (string? memberID = null, string? cellPhoneNumber = null)

Get redeemed static vouchers

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
    public class FetchRedeemedVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var memberID = "memberID_example";  // string? |  (optional) 
            var cellPhoneNumber = "cellPhoneNumber_example";  // string? |  (optional) 

            try
            {
                // Get redeemed static vouchers
                List<StaticVoucher> result = apiInstance.FetchRedeemedVouchers(memberID, cellPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.FetchRedeemedVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchRedeemedVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redeemed static vouchers
    ApiResponse<List<StaticVoucher>> response = apiInstance.FetchRedeemedVouchersWithHttpInfo(memberID, cellPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.FetchRedeemedVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **memberID** | **string?** |  | [optional]  |
| **cellPhoneNumber** | **string?** |  | [optional]  |

### Return type

[**List&lt;StaticVoucher&gt;**](StaticVoucher.md)

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

<a id="fetchrefundedvouchers"></a>
# **FetchRefundedVouchers**
> List&lt;StaticVoucher&gt; FetchRefundedVouchers (string? memberID = null, string? cellPhoneNumber = null)

Get refunded static vouchers

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
    public class FetchRefundedVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var memberID = "memberID_example";  // string? |  (optional) 
            var cellPhoneNumber = "cellPhoneNumber_example";  // string? |  (optional) 

            try
            {
                // Get refunded static vouchers
                List<StaticVoucher> result = apiInstance.FetchRefundedVouchers(memberID, cellPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.FetchRefundedVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchRefundedVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refunded static vouchers
    ApiResponse<List<StaticVoucher>> response = apiInstance.FetchRefundedVouchersWithHttpInfo(memberID, cellPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.FetchRefundedVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **memberID** | **string?** |  | [optional]  |
| **cellPhoneNumber** | **string?** |  | [optional]  |

### Return type

[**List&lt;StaticVoucher&gt;**](StaticVoucher.md)

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

<a id="fetchupcomingvouchers"></a>
# **FetchUpcomingVouchers**
> List&lt;StaticVoucher&gt; FetchUpcomingVouchers (string? memberID = null, string? cellPhoneNumber = null)

Get upcoming static vouchers

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
    public class FetchUpcomingVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var memberID = "memberID_example";  // string? |  (optional) 
            var cellPhoneNumber = "cellPhoneNumber_example";  // string? |  (optional) 

            try
            {
                // Get upcoming static vouchers
                List<StaticVoucher> result = apiInstance.FetchUpcomingVouchers(memberID, cellPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.FetchUpcomingVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchUpcomingVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get upcoming static vouchers
    ApiResponse<List<StaticVoucher>> response = apiInstance.FetchUpcomingVouchersWithHttpInfo(memberID, cellPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.FetchUpcomingVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **memberID** | **string?** |  | [optional]  |
| **cellPhoneNumber** | **string?** |  | [optional]  |

### Return type

[**List&lt;StaticVoucher&gt;**](StaticVoucher.md)

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

<a id="fetchwalletviewsforsession"></a>
# **FetchWalletViewsForSession**
> List&lt;WalletPageView&gt; FetchWalletViewsForSession (string id)

Get Wallet Views for Session

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
    public class FetchWalletViewsForSessionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Get Wallet Views for Session
                List<WalletPageView> result = apiInstance.FetchWalletViewsForSession(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.FetchWalletViewsForSession: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletViewsForSessionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Wallet Views for Session
    ApiResponse<List<WalletPageView>> response = apiInstance.FetchWalletViewsForSessionWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.FetchWalletViewsForSessionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**List&lt;WalletPageView&gt;**](WalletPageView.md)

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

<a id="searchbymemberid"></a>
# **SearchByMemberID**
> Object SearchByMemberID (WTCustomerSearchByMemberID wTCustomerSearchByMemberID)

Find members with memberID

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
    public class SearchByMemberIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var wTCustomerSearchByMemberID = new WTCustomerSearchByMemberID(); // WTCustomerSearchByMemberID | 

            try
            {
                // Find members with memberID
                Object result = apiInstance.SearchByMemberID(wTCustomerSearchByMemberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.SearchByMemberID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchByMemberIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Find members with memberID
    ApiResponse<Object> response = apiInstance.SearchByMemberIDWithHttpInfo(wTCustomerSearchByMemberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.SearchByMemberIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTCustomerSearchByMemberID** | [**WTCustomerSearchByMemberID**](WTCustomerSearchByMemberID.md) |  |  |

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

<a id="searchbyphonenumber"></a>
# **SearchByPhoneNumber**
> Object SearchByPhoneNumber (WTCustomerSearchByPhoneNumber wTCustomerSearchByPhoneNumber)

Find members with phone number

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
    public class SearchByPhoneNumberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CustomerApi(httpClient, config, httpClientHandler);
            var wTCustomerSearchByPhoneNumber = new WTCustomerSearchByPhoneNumber(); // WTCustomerSearchByPhoneNumber | 

            try
            {
                // Find members with phone number
                Object result = apiInstance.SearchByPhoneNumber(wTCustomerSearchByPhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomerApi.SearchByPhoneNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchByPhoneNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Find members with phone number
    ApiResponse<Object> response = apiInstance.SearchByPhoneNumberWithHttpInfo(wTCustomerSearchByPhoneNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomerApi.SearchByPhoneNumberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTCustomerSearchByPhoneNumber** | [**WTCustomerSearchByPhoneNumber**](WTCustomerSearchByPhoneNumber.md) |  |  |

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

