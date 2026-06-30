# WalletInc.Api.ShopifyTerminalApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchWalletItemFromShopifyTerminal**](ShopifyTerminalApi.md#fetchwalletitemfromshopifyterminal) | **GET** /v2/pos/shopify/item/{itemID} | Get item |
| [**RedeemWalletItemFromShopifyTerminal**](ShopifyTerminalApi.md#redeemwalletitemfromshopifyterminal) | **POST** /v2/pos/shopify/item/redeem/{itemID} | Redeem item |
| [**RefundWalletItemFromShopifyTerminal**](ShopifyTerminalApi.md#refundwalletitemfromshopifyterminal) | **POST** /v2/pos/shopify/item/refund/{ledgerEntryID} | Refund transaction |

<a id="fetchwalletitemfromshopifyterminal"></a>
# **FetchWalletItemFromShopifyTerminal**
> Object FetchWalletItemFromShopifyTerminal (string itemID)

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
    public class FetchWalletItemFromShopifyTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ShopifyTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 

            try
            {
                // Get item
                Object result = apiInstance.FetchWalletItemFromShopifyTerminal(itemID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShopifyTerminalApi.FetchWalletItemFromShopifyTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletItemFromShopifyTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get item
    ApiResponse<Object> response = apiInstance.FetchWalletItemFromShopifyTerminalWithHttpInfo(itemID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShopifyTerminalApi.FetchWalletItemFromShopifyTerminalWithHttpInfo: " + e.Message);
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

<a id="redeemwalletitemfromshopifyterminal"></a>
# **RedeemWalletItemFromShopifyTerminal**
> Object RedeemWalletItemFromShopifyTerminal (string itemID, WTWalletItemRedemption wTWalletItemRedemption)

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
    public class RedeemWalletItemFromShopifyTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ShopifyTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 
            var wTWalletItemRedemption = new WTWalletItemRedemption(); // WTWalletItemRedemption | 

            try
            {
                // Redeem item
                Object result = apiInstance.RedeemWalletItemFromShopifyTerminal(itemID, wTWalletItemRedemption);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShopifyTerminalApi.RedeemWalletItemFromShopifyTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedeemWalletItemFromShopifyTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Redeem item
    ApiResponse<Object> response = apiInstance.RedeemWalletItemFromShopifyTerminalWithHttpInfo(itemID, wTWalletItemRedemption);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShopifyTerminalApi.RedeemWalletItemFromShopifyTerminalWithHttpInfo: " + e.Message);
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

<a id="refundwalletitemfromshopifyterminal"></a>
# **RefundWalletItemFromShopifyTerminal**
> Object RefundWalletItemFromShopifyTerminal (string ledgerEntryID)

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
    public class RefundWalletItemFromShopifyTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ShopifyTerminalApi(httpClient, config, httpClientHandler);
            var ledgerEntryID = "ledgerEntryID_example";  // string | 

            try
            {
                // Refund transaction
                Object result = apiInstance.RefundWalletItemFromShopifyTerminal(ledgerEntryID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ShopifyTerminalApi.RefundWalletItemFromShopifyTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundWalletItemFromShopifyTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refund transaction
    ApiResponse<Object> response = apiInstance.RefundWalletItemFromShopifyTerminalWithHttpInfo(ledgerEntryID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ShopifyTerminalApi.RefundWalletItemFromShopifyTerminalWithHttpInfo: " + e.Message);
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

