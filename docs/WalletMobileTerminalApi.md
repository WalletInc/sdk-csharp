# WalletInc.Api.WalletMobileTerminalApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchWalletItemFromMobileTerminal**](WalletMobileTerminalApi.md#fetchwalletitemfrommobileterminal) | **GET** /v2/pos/mobile/item/{itemID} | Get item |
| [**FindMemberByID**](WalletMobileTerminalApi.md#findmemberbyid) | **GET** /v2/pos/mobile/member/{memberID} | Search for Member&#39;s rewards |
| [**RedeemWalletItemFromMobileTerminal**](WalletMobileTerminalApi.md#redeemwalletitemfrommobileterminal) | **POST** /v2/pos/mobile/item/redeem/{itemID} | Redeem item |

<a id="fetchwalletitemfrommobileterminal"></a>
# **FetchWalletItemFromMobileTerminal**
> Object FetchWalletItemFromMobileTerminal (string itemID)

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
    public class FetchWalletItemFromMobileTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletMobileTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 

            try
            {
                // Get item
                Object result = apiInstance.FetchWalletItemFromMobileTerminal(itemID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletMobileTerminalApi.FetchWalletItemFromMobileTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchWalletItemFromMobileTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get item
    ApiResponse<Object> response = apiInstance.FetchWalletItemFromMobileTerminalWithHttpInfo(itemID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletMobileTerminalApi.FetchWalletItemFromMobileTerminalWithHttpInfo: " + e.Message);
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

<a id="findmemberbyid"></a>
# **FindMemberByID**
> Member FindMemberByID (string memberID)

Search for Member's rewards

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
    public class FindMemberByIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletMobileTerminalApi(httpClient, config, httpClientHandler);
            var memberID = "memberID_example";  // string | 

            try
            {
                // Search for Member's rewards
                Member result = apiInstance.FindMemberByID(memberID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletMobileTerminalApi.FindMemberByID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FindMemberByIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search for Member's rewards
    ApiResponse<Member> response = apiInstance.FindMemberByIDWithHttpInfo(memberID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletMobileTerminalApi.FindMemberByIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **memberID** | **string** |  |  |

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
| **401** | Authentication Failed |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redeemwalletitemfrommobileterminal"></a>
# **RedeemWalletItemFromMobileTerminal**
> Object RedeemWalletItemFromMobileTerminal (string itemID, WTWalletItemRedemption wTWalletItemRedemption)

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
    public class RedeemWalletItemFromMobileTerminalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletMobileTerminalApi(httpClient, config, httpClientHandler);
            var itemID = "itemID_example";  // string | 
            var wTWalletItemRedemption = new WTWalletItemRedemption(); // WTWalletItemRedemption | 

            try
            {
                // Redeem item
                Object result = apiInstance.RedeemWalletItemFromMobileTerminal(itemID, wTWalletItemRedemption);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletMobileTerminalApi.RedeemWalletItemFromMobileTerminal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedeemWalletItemFromMobileTerminalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Redeem item
    ApiResponse<Object> response = apiInstance.RedeemWalletItemFromMobileTerminalWithHttpInfo(itemID, wTWalletItemRedemption);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletMobileTerminalApi.RedeemWalletItemFromMobileTerminalWithHttpInfo: " + e.Message);
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

