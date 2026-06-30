# WalletInc.Api.WooCommerceTerminalApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchWalletItemFromWooCommerceTerminal**](WooCommerceTerminalApi.md#fetchwalletitemfromwoocommerceterminal) | **GET** /v2/pos/woocommerce/item/{itemID} | Get item |
| [**RedeemWalletItemFromWooCommerceTerminal**](WooCommerceTerminalApi.md#redeemwalletitemfromwoocommerceterminal) | **POST** /v2/pos/woocommerce/item/redeem/{itemID} | Redeem item |
| [**RefundWalletItemFromWooCommerceTerminal**](WooCommerceTerminalApi.md#refundwalletitemfromwoocommerceterminal) | **POST** /v2/pos/woocommerce/item/refund/{ledgerEntryID} | Refund transaction |

<a id="fetchwalletitemfromwoocommerceterminal"></a>
# **FetchWalletItemFromWooCommerceTerminal**
> Object FetchWalletItemFromWooCommerceTerminal (string itemID)

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
    public class FetchWalletItemFromWooCommerceTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WooCommerceTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 

            try
            {
                // Get item
                Object result = apiInstance.FetchWalletItemFromWooCommerceTerminal(itemID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WooCommerceTerminalApi.FetchWalletItemFromWooCommerceTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletItemFromWooCommerceTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get item
    ApiResponse<Object> response = apiInstance.FetchWalletItemFromWooCommerceTerminalWithHttpInfo(itemID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WooCommerceTerminalApi.FetchWalletItemFromWooCommerceTerminalWithHttpInfo: " + e.Message);
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

<a id="redeemwalletitemfromwoocommerceterminal"></a>
# **RedeemWalletItemFromWooCommerceTerminal**
> Object RedeemWalletItemFromWooCommerceTerminal (string itemID, WTWalletItemRedemption wTWalletItemRedemption)

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
    public class RedeemWalletItemFromWooCommerceTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WooCommerceTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 
            var wTWalletItemRedemption = new WTWalletItemRedemption(); // WTWalletItemRedemption | 

            try
            {
                // Redeem item
                Object result = apiInstance.RedeemWalletItemFromWooCommerceTerminal(itemID, wTWalletItemRedemption);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WooCommerceTerminalApi.RedeemWalletItemFromWooCommerceTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedeemWalletItemFromWooCommerceTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Redeem item
    ApiResponse<Object> response = apiInstance.RedeemWalletItemFromWooCommerceTerminalWithHttpInfo(itemID, wTWalletItemRedemption);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WooCommerceTerminalApi.RedeemWalletItemFromWooCommerceTerminalWithHttpInfo: " + e.Message);
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

<a id="refundwalletitemfromwoocommerceterminal"></a>
# **RefundWalletItemFromWooCommerceTerminal**
> Object RefundWalletItemFromWooCommerceTerminal (string ledgerEntryID)

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
    public class RefundWalletItemFromWooCommerceTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WooCommerceTerminalApi(httpClient, config, httpClientHandler);
            var ledgerEntryID = "ledgerEntryID_example";  // string | 

            try
            {
                // Refund transaction
                Object result = apiInstance.RefundWalletItemFromWooCommerceTerminal(ledgerEntryID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WooCommerceTerminalApi.RefundWalletItemFromWooCommerceTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundWalletItemFromWooCommerceTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refund transaction
    ApiResponse<Object> response = apiInstance.RefundWalletItemFromWooCommerceTerminalWithHttpInfo(ledgerEntryID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WooCommerceTerminalApi.RefundWalletItemFromWooCommerceTerminalWithHttpInfo: " + e.Message);
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

