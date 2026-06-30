# WalletInc.Api.WalletWebTerminalApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchWalletItemFromWebTerminal**](WalletWebTerminalApi.md#fetchwalletitemfromwebterminal) | **GET** /v2/pos/web/item/{itemID} | Get item |
| [**RedeemWalletItemFromWebTerminal**](WalletWebTerminalApi.md#redeemwalletitemfromwebterminal) | **POST** /v2/pos/web/item/redeem/{itemID} | Redeem item |
| [**RefundWalletItemFromWebTerminal**](WalletWebTerminalApi.md#refundwalletitemfromwebterminal) | **POST** /v2/pos/web/item/refund/{ledgerEntryID} | Refund transaction |

<a id="fetchwalletitemfromwebterminal"></a>
# **FetchWalletItemFromWebTerminal**
> Object FetchWalletItemFromWebTerminal (string itemID)

Get item

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
    public class FetchWalletItemFromWebTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletWebTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 

            try
            {
                // Get item
                Object result = apiInstance.FetchWalletItemFromWebTerminal(itemID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletWebTerminalApi.FetchWalletItemFromWebTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletItemFromWebTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get item
    ApiResponse<Object> response = apiInstance.FetchWalletItemFromWebTerminalWithHttpInfo(itemID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletWebTerminalApi.FetchWalletItemFromWebTerminalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemID** | **string** |  |  |

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

<a id="redeemwalletitemfromwebterminal"></a>
# **RedeemWalletItemFromWebTerminal**
> Object RedeemWalletItemFromWebTerminal (string itemID, WTWalletItemRedemption wTWalletItemRedemption)

Redeem item

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
    public class RedeemWalletItemFromWebTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletWebTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 
            var wTWalletItemRedemption = new WTWalletItemRedemption(); // WTWalletItemRedemption | 

            try
            {
                // Redeem item
                Object result = apiInstance.RedeemWalletItemFromWebTerminal(itemID, wTWalletItemRedemption);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletWebTerminalApi.RedeemWalletItemFromWebTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedeemWalletItemFromWebTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Redeem item
    ApiResponse<Object> response = apiInstance.RedeemWalletItemFromWebTerminalWithHttpInfo(itemID, wTWalletItemRedemption);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletWebTerminalApi.RedeemWalletItemFromWebTerminalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemID** | **string** |  |  |
| **wTWalletItemRedemption** | [**WTWalletItemRedemption**](WTWalletItemRedemption.md) |  |  |

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

<a id="refundwalletitemfromwebterminal"></a>
# **RefundWalletItemFromWebTerminal**
> Object RefundWalletItemFromWebTerminal (string ledgerEntryID)

Refund transaction

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
    public class RefundWalletItemFromWebTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletWebTerminalApi(httpClient, config, httpClientHandler);
            var ledgerEntryID = "ledgerEntryID_example";  // string | 

            try
            {
                // Refund transaction
                Object result = apiInstance.RefundWalletItemFromWebTerminal(ledgerEntryID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletWebTerminalApi.RefundWalletItemFromWebTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundWalletItemFromWebTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refund transaction
    ApiResponse<Object> response = apiInstance.RefundWalletItemFromWebTerminalWithHttpInfo(ledgerEntryID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletWebTerminalApi.RefundWalletItemFromWebTerminalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ledgerEntryID** | **string** |  |  |

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

