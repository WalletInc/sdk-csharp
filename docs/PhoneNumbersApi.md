# WalletInc.Api.PhoneNumbersApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AcquirePhoneNumber**](PhoneNumbersApi.md#acquirephonenumber) | **POST** /v2/sms/phoneNumber/acquire | Acquire phone number |
| [**ArchivePhoneNumber**](PhoneNumbersApi.md#archivephonenumber) | **DELETE** /v2/sms/phoneNumber/{phoneNumberID} | Archive phone number |
| [**FetchBlockedTCPAEntries**](PhoneNumbersApi.md#fetchblockedtcpaentries) | **GET** /v2/sms/phoneNumber/blocked/{phoneNumberID} | Get blocked TCPA entries |
| [**FetchMerchantPhoneNumbers**](PhoneNumbersApi.md#fetchmerchantphonenumbers) | **GET** /v2/merchant/phoneNumbers/all | Get all phone numbers |
| [**FetchPhoneNumber**](PhoneNumbersApi.md#fetchphonenumber) | **GET** /v2/merchant/phoneNumber/{phoneNumberID} | Get phone number |
| [**FetchSMSAgreement**](PhoneNumbersApi.md#fetchsmsagreement) | **GET** /v2/sms/agreement | Get SMS Agreement |
| [**FetchTCPAFilter**](PhoneNumbersApi.md#fetchtcpafilter) | **GET** /v2/merchant/tcpa/filter/all | Get all TCPA Filters |
| [**RestorePhoneNumber**](PhoneNumbersApi.md#restorephonenumber) | **PATCH** /v2/sms/phoneNumber/{phoneNumberID} | Restore phone number |
| [**SendPhoneNumberForVerification**](PhoneNumbersApi.md#sendphonenumberforverification) | **PUT** /v2/sms/phoneNumber/verification/{phoneNumberID} | Request phone number verification |
| [**UpdatePhoneNumber**](PhoneNumbersApi.md#updatephonenumber) | **PUT** /v2/sms/phoneNumber/{phoneNumberID} | Update phone number |

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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var wTSMSAcquirePhoneNumber = new WTSMSAcquirePhoneNumber(); // WTSMSAcquirePhoneNumber | 

            try
            {
                // Acquire phone number
                PhoneNumber result = apiInstance.AcquirePhoneNumber(wTSMSAcquirePhoneNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.AcquirePhoneNumber: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.AcquirePhoneNumberWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Archive phone number
                PhoneNumber result = apiInstance.ArchivePhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.ArchivePhoneNumber: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.ArchivePhoneNumberWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get blocked TCPA entries
                List<Tcpa> result = apiInstance.FetchBlockedTCPAEntries(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.FetchBlockedTCPAEntries: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.FetchBlockedTCPAEntriesWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling PhoneNumbersApi.FetchMerchantPhoneNumbers: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.FetchMerchantPhoneNumbersWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Get phone number
                PhoneNumber result = apiInstance.FetchPhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.FetchPhoneNumber: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.FetchPhoneNumberWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);

            try
            {
                // Get SMS Agreement
                Object result = apiInstance.FetchSMSAgreement();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.FetchSMSAgreement: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.FetchSMSAgreementWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);

            try
            {
                // Get all TCPA Filters
                List<Tcpa> result = apiInstance.FetchTCPAFilter();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.FetchTCPAFilter: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.FetchTCPAFilterWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
            var phoneNumberID = "phoneNumberID_example";  // string | 

            try
            {
                // Restore phone number
                PhoneNumber result = apiInstance.RestorePhoneNumber(phoneNumberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PhoneNumbersApi.RestorePhoneNumber: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.RestorePhoneNumberWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling PhoneNumbersApi.SendPhoneNumberForVerification: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.SendPhoneNumberForVerificationWithHttpInfo: " + e.Message);
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
            var apiInstance = new PhoneNumbersApi(httpClient, config, httpClientHandler);
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
                Debug.Print("Exception when calling PhoneNumbersApi.UpdatePhoneNumber: " + e.Message);
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
    Debug.Print("Exception when calling PhoneNumbersApi.UpdatePhoneNumberWithHttpInfo: " + e.Message);
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

