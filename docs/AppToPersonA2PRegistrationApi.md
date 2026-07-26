# WalletInc.Api.AppToPersonA2PRegistrationApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BeginA2PApplication**](AppToPersonA2PRegistrationApi.md#begina2papplication) | **POST** /v2/a2p/application | Create A2P Application |
| [**BeginA2PApplicationGovernment**](AppToPersonA2PRegistrationApi.md#begina2papplicationgovernment) | **POST** /a2p/application/government | Begin A2P Application (Government) |
| [**BeginA2PApplicationNonProfit**](AppToPersonA2PRegistrationApi.md#begina2papplicationnonprofit) | **POST** /a2p/application/nonprofit | Begin A2P Application (Non-profit) |
| [**BeginA2PApplicationPublic**](AppToPersonA2PRegistrationApi.md#begina2papplicationpublic) | **POST** /a2p/application/public | Begin A2P Application (Public: a publicly-traded company; requires stock exchange, ticker, and brand contact email) |
| [**BeginA2PApplicationSoleProprietor**](AppToPersonA2PRegistrationApi.md#begina2papplicationsoleproprietor) | **POST** /a2p/application/sole-proprietor | Begin A2P Application (Sole Proprietor: no EIN; requires a mobile number for OTP verification) |
| [**BeginA2PApplicationStandard**](AppToPersonA2PRegistrationApi.md#begina2papplicationstandard) | **POST** /a2p/application/standard | Begin A2P Application (Standard: a private, for-profit business with an EIN) |
| [**FetchA2PApplication**](AppToPersonA2PRegistrationApi.md#fetcha2papplication) | **GET** /v2/a2p/application | Get A2P Application |
| [**FetchA2PRegistration**](AppToPersonA2PRegistrationApi.md#fetcha2pregistration) | **GET** /v2/a2p/registration | Get A2P Registration |
| [**UpdateA2PApplication**](AppToPersonA2PRegistrationApi.md#updatea2papplication) | **PUT** /v2/a2p/application/{applicationID} | Update A2P Application |

<a id="begina2papplication"></a>
# **BeginA2PApplication**
> bool BeginA2PApplication (A2PApplicationSubmission a2PApplicationSubmission)

Create A2P Application

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
    public class BeginA2PApplicationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);
            var a2PApplicationSubmission = new A2PApplicationSubmission(); // A2PApplicationSubmission | 

            try
            {
                // Create A2P Application
                bool result = apiInstance.BeginA2PApplication(a2PApplicationSubmission);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplication: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BeginA2PApplicationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create A2P Application
    ApiResponse<bool> response = apiInstance.BeginA2PApplicationWithHttpInfo(a2PApplicationSubmission);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **a2PApplicationSubmission** | [**A2PApplicationSubmission**](A2PApplicationSubmission.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="begina2papplicationgovernment"></a>
# **BeginA2PApplicationGovernment**
> bool BeginA2PApplicationGovernment (A2PGovernmentSubmission a2PGovernmentSubmission)

Begin A2P Application (Government)

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
    public class BeginA2PApplicationGovernmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);
            var a2PGovernmentSubmission = new A2PGovernmentSubmission(); // A2PGovernmentSubmission | 

            try
            {
                // Begin A2P Application (Government)
                bool result = apiInstance.BeginA2PApplicationGovernment(a2PGovernmentSubmission);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationGovernment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BeginA2PApplicationGovernmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Begin A2P Application (Government)
    ApiResponse<bool> response = apiInstance.BeginA2PApplicationGovernmentWithHttpInfo(a2PGovernmentSubmission);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationGovernmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **a2PGovernmentSubmission** | [**A2PGovernmentSubmission**](A2PGovernmentSubmission.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="begina2papplicationnonprofit"></a>
# **BeginA2PApplicationNonProfit**
> bool BeginA2PApplicationNonProfit (A2PNonProfitSubmission a2PNonProfitSubmission)

Begin A2P Application (Non-profit)

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
    public class BeginA2PApplicationNonProfitExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);
            var a2PNonProfitSubmission = new A2PNonProfitSubmission(); // A2PNonProfitSubmission | 

            try
            {
                // Begin A2P Application (Non-profit)
                bool result = apiInstance.BeginA2PApplicationNonProfit(a2PNonProfitSubmission);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationNonProfit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BeginA2PApplicationNonProfitWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Begin A2P Application (Non-profit)
    ApiResponse<bool> response = apiInstance.BeginA2PApplicationNonProfitWithHttpInfo(a2PNonProfitSubmission);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationNonProfitWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **a2PNonProfitSubmission** | [**A2PNonProfitSubmission**](A2PNonProfitSubmission.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="begina2papplicationpublic"></a>
# **BeginA2PApplicationPublic**
> bool BeginA2PApplicationPublic (A2PPublicSubmission a2PPublicSubmission)

Begin A2P Application (Public: a publicly-traded company; requires stock exchange, ticker, and brand contact email)

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
    public class BeginA2PApplicationPublicExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);
            var a2PPublicSubmission = new A2PPublicSubmission(); // A2PPublicSubmission | 

            try
            {
                // Begin A2P Application (Public: a publicly-traded company; requires stock exchange, ticker, and brand contact email)
                bool result = apiInstance.BeginA2PApplicationPublic(a2PPublicSubmission);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationPublic: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BeginA2PApplicationPublicWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Begin A2P Application (Public: a publicly-traded company; requires stock exchange, ticker, and brand contact email)
    ApiResponse<bool> response = apiInstance.BeginA2PApplicationPublicWithHttpInfo(a2PPublicSubmission);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationPublicWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **a2PPublicSubmission** | [**A2PPublicSubmission**](A2PPublicSubmission.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="begina2papplicationsoleproprietor"></a>
# **BeginA2PApplicationSoleProprietor**
> bool BeginA2PApplicationSoleProprietor (A2PSoleProprietorSubmission a2PSoleProprietorSubmission)

Begin A2P Application (Sole Proprietor: no EIN; requires a mobile number for OTP verification)

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
    public class BeginA2PApplicationSoleProprietorExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);
            var a2PSoleProprietorSubmission = new A2PSoleProprietorSubmission(); // A2PSoleProprietorSubmission | 

            try
            {
                // Begin A2P Application (Sole Proprietor: no EIN; requires a mobile number for OTP verification)
                bool result = apiInstance.BeginA2PApplicationSoleProprietor(a2PSoleProprietorSubmission);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationSoleProprietor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BeginA2PApplicationSoleProprietorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Begin A2P Application (Sole Proprietor: no EIN; requires a mobile number for OTP verification)
    ApiResponse<bool> response = apiInstance.BeginA2PApplicationSoleProprietorWithHttpInfo(a2PSoleProprietorSubmission);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationSoleProprietorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **a2PSoleProprietorSubmission** | [**A2PSoleProprietorSubmission**](A2PSoleProprietorSubmission.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="begina2papplicationstandard"></a>
# **BeginA2PApplicationStandard**
> bool BeginA2PApplicationStandard (A2PStandardSubmission a2PStandardSubmission)

Begin A2P Application (Standard: a private, for-profit business with an EIN)

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
    public class BeginA2PApplicationStandardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);
            var a2PStandardSubmission = new A2PStandardSubmission(); // A2PStandardSubmission | 

            try
            {
                // Begin A2P Application (Standard: a private, for-profit business with an EIN)
                bool result = apiInstance.BeginA2PApplicationStandard(a2PStandardSubmission);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationStandard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BeginA2PApplicationStandardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Begin A2P Application (Standard: a private, for-profit business with an EIN)
    ApiResponse<bool> response = apiInstance.BeginA2PApplicationStandardWithHttpInfo(a2PStandardSubmission);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.BeginA2PApplicationStandardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **a2PStandardSubmission** | [**A2PStandardSubmission**](A2PStandardSubmission.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="fetcha2papplication"></a>
# **FetchA2PApplication**
> Object FetchA2PApplication ()

Get A2P Application

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
    public class FetchA2PApplicationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);

            try
            {
                // Get A2P Application
                Object result = apiInstance.FetchA2PApplication();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.FetchA2PApplication: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchA2PApplicationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get A2P Application
    ApiResponse<Object> response = apiInstance.FetchA2PApplicationWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.FetchA2PApplicationWithHttpInfo: " + e.Message);
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

<a id="fetcha2pregistration"></a>
# **FetchA2PRegistration**
> Object FetchA2PRegistration ()

Get A2P Registration

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
    public class FetchA2PRegistrationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);

            try
            {
                // Get A2P Registration
                Object result = apiInstance.FetchA2PRegistration();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.FetchA2PRegistration: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchA2PRegistrationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get A2P Registration
    ApiResponse<Object> response = apiInstance.FetchA2PRegistrationWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.FetchA2PRegistrationWithHttpInfo: " + e.Message);
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

<a id="updatea2papplication"></a>
# **UpdateA2PApplication**
> bool UpdateA2PApplication (string applicationID, WTA2PApplicationUpdateParams wTA2PApplicationUpdateParams)

Update A2P Application

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
    public class UpdateA2PApplicationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new AppToPersonA2PRegistrationApi(httpClient, config, httpClientHandler);
            var applicationID = "applicationID_example";  // string | 
            var wTA2PApplicationUpdateParams = new WTA2PApplicationUpdateParams(); // WTA2PApplicationUpdateParams | 

            try
            {
                // Update A2P Application
                bool result = apiInstance.UpdateA2PApplication(applicationID, wTA2PApplicationUpdateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.UpdateA2PApplication: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateA2PApplicationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update A2P Application
    ApiResponse<bool> response = apiInstance.UpdateA2PApplicationWithHttpInfo(applicationID, wTA2PApplicationUpdateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppToPersonA2PRegistrationApi.UpdateA2PApplicationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **applicationID** | **string** |  |  |
| **wTA2PApplicationUpdateParams** | [**WTA2PApplicationUpdateParams**](WTA2PApplicationUpdateParams.md) |  |  |

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
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

