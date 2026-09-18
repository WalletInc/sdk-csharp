# WalletInc.Api.WalletConfigurationApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchPassStyle**](WalletConfigurationApi.md#fetchpassstyle) | **GET** /wallet/passStyle | Get pass styling |
| [**GenerateAndroidKeystore**](WalletConfigurationApi.md#generateandroidkeystore) | **POST** /v2/wallet/android/keystore | Generate Android TWA signing keystore |
| [**ResetPassStyle**](WalletConfigurationApi.md#resetpassstyle) | **DELETE** /wallet/passStyle/{provider} | Reset one provider&#39;s pass styling |
| [**SaveMerchantCreditPaymentDesign**](WalletConfigurationApi.md#savemerchantcreditpaymentdesign) | **PUT** /v2/wallet/merchantCredit/paymentDesign | Update payment design for merchant credits |
| [**SaveWalletRecord**](WalletConfigurationApi.md#savewalletrecord) | **PUT** /v2/wallet | Update wallet record |

<a id="fetchpassstyle"></a>
# **FetchPassStyle**
> WTPassStyleResponse FetchPassStyle ()

Get pass styling

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
    public class FetchPassStyleExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletConfigurationApi(httpClient, config, httpClientHandler);

            try
            {
                // Get pass styling
                WTPassStyleResponse result = apiInstance.FetchPassStyle();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletConfigurationApi.FetchPassStyle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchPassStyleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get pass styling
    ApiResponse<WTPassStyleResponse> response = apiInstance.FetchPassStyleWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletConfigurationApi.FetchPassStyleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**WTPassStyleResponse**](WTPassStyleResponse.md)

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

<a id="generateandroidkeystore"></a>
# **GenerateAndroidKeystore**
> WTAndroidKeystoreResponse GenerateAndroidKeystore (bool? regenerate = null)

Generate Android TWA signing keystore

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
    public class GenerateAndroidKeystoreExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletConfigurationApi(httpClient, config, httpClientHandler);
            var regenerate = true;  // bool? |  (optional) 

            try
            {
                // Generate Android TWA signing keystore
                WTAndroidKeystoreResponse result = apiInstance.GenerateAndroidKeystore(regenerate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletConfigurationApi.GenerateAndroidKeystore: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GenerateAndroidKeystoreWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generate Android TWA signing keystore
    ApiResponse<WTAndroidKeystoreResponse> response = apiInstance.GenerateAndroidKeystoreWithHttpInfo(regenerate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletConfigurationApi.GenerateAndroidKeystoreWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **regenerate** | **bool?** |  | [optional]  |

### Return type

[**WTAndroidKeystoreResponse**](WTAndroidKeystoreResponse.md)

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

<a id="resetpassstyle"></a>
# **ResetPassStyle**
> WTPassStyleResponse ResetPassStyle (WTWalletPassProvider provider)

Reset one provider's pass styling

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
    public class ResetPassStyleExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletConfigurationApi(httpClient, config, httpClientHandler);
            var provider = (WTWalletPassProvider) "google";  // WTWalletPassProvider | 

            try
            {
                // Reset one provider's pass styling
                WTPassStyleResponse result = apiInstance.ResetPassStyle(provider);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletConfigurationApi.ResetPassStyle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetPassStyleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reset one provider's pass styling
    ApiResponse<WTPassStyleResponse> response = apiInstance.ResetPassStyleWithHttpInfo(provider);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletConfigurationApi.ResetPassStyleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **provider** | **WTWalletPassProvider** |  |  |

### Return type

[**WTPassStyleResponse**](WTPassStyleResponse.md)

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

<a id="savemerchantcreditpaymentdesign"></a>
# **SaveMerchantCreditPaymentDesign**
> Object SaveMerchantCreditPaymentDesign (SaveMerchantCreditPaymentDesignRequest saveMerchantCreditPaymentDesignRequest)

Update payment design for merchant credits

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
    public class SaveMerchantCreditPaymentDesignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletConfigurationApi(httpClient, config, httpClientHandler);
            var saveMerchantCreditPaymentDesignRequest = new SaveMerchantCreditPaymentDesignRequest(); // SaveMerchantCreditPaymentDesignRequest | 

            try
            {
                // Update payment design for merchant credits
                Object result = apiInstance.SaveMerchantCreditPaymentDesign(saveMerchantCreditPaymentDesignRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletConfigurationApi.SaveMerchantCreditPaymentDesign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveMerchantCreditPaymentDesignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update payment design for merchant credits
    ApiResponse<Object> response = apiInstance.SaveMerchantCreditPaymentDesignWithHttpInfo(saveMerchantCreditPaymentDesignRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletConfigurationApi.SaveMerchantCreditPaymentDesignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **saveMerchantCreditPaymentDesignRequest** | [**SaveMerchantCreditPaymentDesignRequest**](SaveMerchantCreditPaymentDesignRequest.md) |  |  |

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

<a id="savewalletrecord"></a>
# **SaveWalletRecord**
> Object SaveWalletRecord (WTWalletConfigurationSaveWalletRecord wTWalletConfigurationSaveWalletRecord)

Update wallet record

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
    public class SaveWalletRecordExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletConfigurationApi(httpClient, config, httpClientHandler);
            var wTWalletConfigurationSaveWalletRecord = new WTWalletConfigurationSaveWalletRecord(); // WTWalletConfigurationSaveWalletRecord | 

            try
            {
                // Update wallet record
                Object result = apiInstance.SaveWalletRecord(wTWalletConfigurationSaveWalletRecord);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletConfigurationApi.SaveWalletRecord: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveWalletRecordWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update wallet record
    ApiResponse<Object> response = apiInstance.SaveWalletRecordWithHttpInfo(wTWalletConfigurationSaveWalletRecord);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletConfigurationApi.SaveWalletRecordWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTWalletConfigurationSaveWalletRecord** | [**WTWalletConfigurationSaveWalletRecord**](WTWalletConfigurationSaveWalletRecord.md) |  |  |

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

