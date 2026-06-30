# WalletInc.Api.WixTerminalApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchWalletItemFromWixTerminal**](WixTerminalApi.md#fetchwalletitemfromwixterminal) | **GET** /v2/pos/wix/item/{itemID} | Get item |
| [**RedeemWalletItemFromWixTerminal**](WixTerminalApi.md#redeemwalletitemfromwixterminal) | **POST** /v2/pos/wix/item/redeem/{itemID} | Redeem item |
| [**RefundWalletItemFromWixTerminal**](WixTerminalApi.md#refundwalletitemfromwixterminal) | **POST** /v2/pos/wix/item/refund/{ledgerEntryID} | Refund transaction |

<a id="fetchwalletitemfromwixterminal"></a>
# **FetchWalletItemFromWixTerminal**
> Object FetchWalletItemFromWixTerminal (string itemID)

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
    public class FetchWalletItemFromWixTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WixTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 

            try
            {
                // Get item
                Object result = apiInstance.FetchWalletItemFromWixTerminal(itemID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WixTerminalApi.FetchWalletItemFromWixTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletItemFromWixTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get item
    ApiResponse<Object> response = apiInstance.FetchWalletItemFromWixTerminalWithHttpInfo(itemID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WixTerminalApi.FetchWalletItemFromWixTerminalWithHttpInfo: " + e.Message);
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

<a id="redeemwalletitemfromwixterminal"></a>
# **RedeemWalletItemFromWixTerminal**
> Object RedeemWalletItemFromWixTerminal (string itemID, WTWalletItemRedemption wTWalletItemRedemption)

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
    public class RedeemWalletItemFromWixTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WixTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 
            var wTWalletItemRedemption = new WTWalletItemRedemption(); // WTWalletItemRedemption | 

            try
            {
                // Redeem item
                Object result = apiInstance.RedeemWalletItemFromWixTerminal(itemID, wTWalletItemRedemption);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WixTerminalApi.RedeemWalletItemFromWixTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedeemWalletItemFromWixTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Redeem item
    ApiResponse<Object> response = apiInstance.RedeemWalletItemFromWixTerminalWithHttpInfo(itemID, wTWalletItemRedemption);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WixTerminalApi.RedeemWalletItemFromWixTerminalWithHttpInfo: " + e.Message);
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

<a id="refundwalletitemfromwixterminal"></a>
# **RefundWalletItemFromWixTerminal**
> Object RefundWalletItemFromWixTerminal (string ledgerEntryID)

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
    public class RefundWalletItemFromWixTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WixTerminalApi(httpClient, config, httpClientHandler);
            var ledgerEntryID = "ledgerEntryID_example";  // string | 

            try
            {
                // Refund transaction
                Object result = apiInstance.RefundWalletItemFromWixTerminal(ledgerEntryID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WixTerminalApi.RefundWalletItemFromWixTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundWalletItemFromWixTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refund transaction
    ApiResponse<Object> response = apiInstance.RefundWalletItemFromWixTerminalWithHttpInfo(ledgerEntryID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WixTerminalApi.RefundWalletItemFromWixTerminalWithHttpInfo: " + e.Message);
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

