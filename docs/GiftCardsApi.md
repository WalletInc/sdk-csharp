# WalletInc.Api.GiftCardsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ClaimGift**](GiftCardsApi.md#claimgift) | **POST** /giftcards/{giftID}/claim | Claim a gifted card or certificate Claims a gift into the recipient&#39;s wallet (guest-to-guest). For a certificate with the gift-redemption requirement, the claimer must be someone other than the purchaser. |
| [**CreateCertificateDeal**](GiftCardsApi.md#createcertificatedeal) | **POST** /giftcards/deals | Create a gift-certificate deal (draft) Creates the discounted \&quot;deal\&quot; template (product/service entitlement, retail + sale price, quantity, validity) as a DRAFT. It is not purchasable until published. Authoring a draft does not require Stripe Connect. |
| [**FetchCertificateDeal**](GiftCardsApi.md#fetchcertificatedeal) | **GET** /giftcards/deals/{dealID} | Fetch a certificate deal by id |
| [**FetchGift**](GiftCardsApi.md#fetchgift) | **GET** /giftcards/{giftID} | Fetch a gift card or certificate by id |
| [**PublishCertificateDeal**](GiftCardsApi.md#publishcertificatedeal) | **POST** /giftcards/deals/{dealID}/publish | Publish a certificate deal (put it on sale) Flips a draft deal live so guests can buy certificates from it. Requires the merchant&#39;s Stripe Connect account to be active (charges enabled), since a purchase is a direct charge to that account. |
| [**PurchaseCertificateFromDeal**](GiftCardsApi.md#purchasecertificatefromdeal) | **POST** /giftcards/deals/{dealID}/purchase | Purchase a certificate from a deal Runs the (mock) Connect direct charge of the deal&#39;s discounted sale price to the merchant, then mints a single-use certificate from the deal. Optionally gifts it to a recipient. |
| [**PurchaseGiftCard**](GiftCardsApi.md#purchasegiftcard) | **POST** /giftcards/purchase | Purchase a gift card Runs the (mock) Connect direct charge to the merchant, then issues a funded, reloadable gift card. Optionally gifts it to a recipient. Requires the merchant&#39;s Stripe Connect account to be active (charges enabled). |

<a id="claimgift"></a>
# **ClaimGift**
> Object ClaimGift (string giftID, WTGiftClaimRequest wTGiftClaimRequest)

Claim a gifted card or certificate Claims a gift into the recipient's wallet (guest-to-guest). For a certificate with the gift-redemption requirement, the claimer must be someone other than the purchaser.

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
    public class ClaimGiftExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GiftCardsApi(httpClient, config, httpClientHandler);
            var giftID = "giftID_example";  // string | 
            var wTGiftClaimRequest = new WTGiftClaimRequest(); // WTGiftClaimRequest | 

            try
            {
                // Claim a gifted card or certificate Claims a gift into the recipient's wallet (guest-to-guest). For a certificate with the gift-redemption requirement, the claimer must be someone other than the purchaser.
                Object result = apiInstance.ClaimGift(giftID, wTGiftClaimRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GiftCardsApi.ClaimGift: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ClaimGiftWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Claim a gifted card or certificate Claims a gift into the recipient's wallet (guest-to-guest). For a certificate with the gift-redemption requirement, the claimer must be someone other than the purchaser.
    ApiResponse<Object> response = apiInstance.ClaimGiftWithHttpInfo(giftID, wTGiftClaimRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GiftCardsApi.ClaimGiftWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **giftID** | **string** |  |  |
| **wTGiftClaimRequest** | [**WTGiftClaimRequest**](WTGiftClaimRequest.md) |  |  |

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

<a id="createcertificatedeal"></a>
# **CreateCertificateDeal**
> Object CreateCertificateDeal (WTCertificateDealCreateRequest wTCertificateDealCreateRequest)

Create a gift-certificate deal (draft) Creates the discounted \"deal\" template (product/service entitlement, retail + sale price, quantity, validity) as a DRAFT. It is not purchasable until published. Authoring a draft does not require Stripe Connect.

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
    public class CreateCertificateDealExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GiftCardsApi(httpClient, config, httpClientHandler);
            var wTCertificateDealCreateRequest = new WTCertificateDealCreateRequest(); // WTCertificateDealCreateRequest | 

            try
            {
                // Create a gift-certificate deal (draft) Creates the discounted \"deal\" template (product/service entitlement, retail + sale price, quantity, validity) as a DRAFT. It is not purchasable until published. Authoring a draft does not require Stripe Connect.
                Object result = apiInstance.CreateCertificateDeal(wTCertificateDealCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GiftCardsApi.CreateCertificateDeal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCertificateDealWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a gift-certificate deal (draft) Creates the discounted \"deal\" template (product/service entitlement, retail + sale price, quantity, validity) as a DRAFT. It is not purchasable until published. Authoring a draft does not require Stripe Connect.
    ApiResponse<Object> response = apiInstance.CreateCertificateDealWithHttpInfo(wTCertificateDealCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GiftCardsApi.CreateCertificateDealWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTCertificateDealCreateRequest** | [**WTCertificateDealCreateRequest**](WTCertificateDealCreateRequest.md) |  |  |

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

<a id="fetchcertificatedeal"></a>
# **FetchCertificateDeal**
> Object FetchCertificateDeal (string dealID)

Fetch a certificate deal by id

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
    public class FetchCertificateDealExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GiftCardsApi(httpClient, config, httpClientHandler);
            var dealID = "dealID_example";  // string | 

            try
            {
                // Fetch a certificate deal by id
                Object result = apiInstance.FetchCertificateDeal(dealID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GiftCardsApi.FetchCertificateDeal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchCertificateDealWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Fetch a certificate deal by id
    ApiResponse<Object> response = apiInstance.FetchCertificateDealWithHttpInfo(dealID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GiftCardsApi.FetchCertificateDealWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dealID** | **string** |  |  |

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

<a id="fetchgift"></a>
# **FetchGift**
> Object FetchGift (string giftID)

Fetch a gift card or certificate by id

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
    public class FetchGiftExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GiftCardsApi(httpClient, config, httpClientHandler);
            var giftID = "giftID_example";  // string | 

            try
            {
                // Fetch a gift card or certificate by id
                Object result = apiInstance.FetchGift(giftID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GiftCardsApi.FetchGift: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchGiftWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Fetch a gift card or certificate by id
    ApiResponse<Object> response = apiInstance.FetchGiftWithHttpInfo(giftID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GiftCardsApi.FetchGiftWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **giftID** | **string** |  |  |

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

<a id="publishcertificatedeal"></a>
# **PublishCertificateDeal**
> Object PublishCertificateDeal (string dealID)

Publish a certificate deal (put it on sale) Flips a draft deal live so guests can buy certificates from it. Requires the merchant's Stripe Connect account to be active (charges enabled), since a purchase is a direct charge to that account.

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
    public class PublishCertificateDealExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GiftCardsApi(httpClient, config, httpClientHandler);
            var dealID = "dealID_example";  // string | 

            try
            {
                // Publish a certificate deal (put it on sale) Flips a draft deal live so guests can buy certificates from it. Requires the merchant's Stripe Connect account to be active (charges enabled), since a purchase is a direct charge to that account.
                Object result = apiInstance.PublishCertificateDeal(dealID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GiftCardsApi.PublishCertificateDeal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PublishCertificateDealWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Publish a certificate deal (put it on sale) Flips a draft deal live so guests can buy certificates from it. Requires the merchant's Stripe Connect account to be active (charges enabled), since a purchase is a direct charge to that account.
    ApiResponse<Object> response = apiInstance.PublishCertificateDealWithHttpInfo(dealID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GiftCardsApi.PublishCertificateDealWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dealID** | **string** |  |  |

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

<a id="purchasecertificatefromdeal"></a>
# **PurchaseCertificateFromDeal**
> Object PurchaseCertificateFromDeal (string dealID, WTCertificatePurchaseRequest wTCertificatePurchaseRequest)

Purchase a certificate from a deal Runs the (mock) Connect direct charge of the deal's discounted sale price to the merchant, then mints a single-use certificate from the deal. Optionally gifts it to a recipient.

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
    public class PurchaseCertificateFromDealExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GiftCardsApi(httpClient, config, httpClientHandler);
            var dealID = "dealID_example";  // string | 
            var wTCertificatePurchaseRequest = new WTCertificatePurchaseRequest(); // WTCertificatePurchaseRequest | 

            try
            {
                // Purchase a certificate from a deal Runs the (mock) Connect direct charge of the deal's discounted sale price to the merchant, then mints a single-use certificate from the deal. Optionally gifts it to a recipient.
                Object result = apiInstance.PurchaseCertificateFromDeal(dealID, wTCertificatePurchaseRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GiftCardsApi.PurchaseCertificateFromDeal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PurchaseCertificateFromDealWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Purchase a certificate from a deal Runs the (mock) Connect direct charge of the deal's discounted sale price to the merchant, then mints a single-use certificate from the deal. Optionally gifts it to a recipient.
    ApiResponse<Object> response = apiInstance.PurchaseCertificateFromDealWithHttpInfo(dealID, wTCertificatePurchaseRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GiftCardsApi.PurchaseCertificateFromDealWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dealID** | **string** |  |  |
| **wTCertificatePurchaseRequest** | [**WTCertificatePurchaseRequest**](WTCertificatePurchaseRequest.md) |  |  |

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

<a id="purchasegiftcard"></a>
# **PurchaseGiftCard**
> Object PurchaseGiftCard (WTGiftCardPurchaseRequest wTGiftCardPurchaseRequest)

Purchase a gift card Runs the (mock) Connect direct charge to the merchant, then issues a funded, reloadable gift card. Optionally gifts it to a recipient. Requires the merchant's Stripe Connect account to be active (charges enabled).

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
    public class PurchaseGiftCardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new GiftCardsApi(httpClient, config, httpClientHandler);
            var wTGiftCardPurchaseRequest = new WTGiftCardPurchaseRequest(); // WTGiftCardPurchaseRequest | 

            try
            {
                // Purchase a gift card Runs the (mock) Connect direct charge to the merchant, then issues a funded, reloadable gift card. Optionally gifts it to a recipient. Requires the merchant's Stripe Connect account to be active (charges enabled).
                Object result = apiInstance.PurchaseGiftCard(wTGiftCardPurchaseRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GiftCardsApi.PurchaseGiftCard: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PurchaseGiftCardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Purchase a gift card Runs the (mock) Connect direct charge to the merchant, then issues a funded, reloadable gift card. Optionally gifts it to a recipient. Requires the merchant's Stripe Connect account to be active (charges enabled).
    ApiResponse<Object> response = apiInstance.PurchaseGiftCardWithHttpInfo(wTGiftCardPurchaseRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GiftCardsApi.PurchaseGiftCardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTGiftCardPurchaseRequest** | [**WTGiftCardPurchaseRequest**](WTGiftCardPurchaseRequest.md) |  |  |

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

