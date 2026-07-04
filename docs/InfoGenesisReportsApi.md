# WalletInc.Api.InfoGenesisReportsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CountAdCreditsRedemptions**](InfoGenesisReportsApi.md#countadcreditsredemptions) | **POST** /v2/pos/infogenesis/count/adCredits/redemptions | Count redeemed ad credits |
| [**CountAdCreditsRefunds**](InfoGenesisReportsApi.md#countadcreditsrefunds) | **POST** /v2/pos/infogenesis/count/adCredits/refunds | Count refunded ad credits |
| [**CountDynamicVoucherRedemptions**](InfoGenesisReportsApi.md#countdynamicvoucherredemptions) | **POST** /v2/pos/infogenesis/count/dynamicVoucher/redemptions | Count dynamic voucher redemptions |
| [**CountDynamicVoucherRefunds**](InfoGenesisReportsApi.md#countdynamicvoucherrefunds) | **POST** /v2/pos/infogenesis/count/dynamicVoucher/refunds | Count dynamic voucher refunds |
| [**CountMembershipPointsRedemptions**](InfoGenesisReportsApi.md#countmembershippointsredemptions) | **POST** /v2/pos/infogenesis/count/membershipPoints/redemptions | Count redeemed membership points |
| [**CountMembershipPointsRefunds**](InfoGenesisReportsApi.md#countmembershippointsrefunds) | **POST** /v2/pos/infogenesis/count/membershipPoints/refunds | Count refunded membership points |
| [**CountMembershipTierRedemptions**](InfoGenesisReportsApi.md#countmembershiptierredemptions) | **POST** /v2/pos/infogenesis/count/membershipTier/redemptions | Count tier redemptions |
| [**CountMembershipTierRefunds**](InfoGenesisReportsApi.md#countmembershiptierrefunds) | **POST** /v2/pos/infogenesis/count/membershipTier/refunds | Count tier refunds |
| [**CountMerchantCreditRedemptions**](InfoGenesisReportsApi.md#countmerchantcreditredemptions) | **POST** /v2/pos/infogenesis/count/merchantCredit/redemptions | Count redeemed merchant credits |
| [**CountMerchantCreditRefunds**](InfoGenesisReportsApi.md#countmerchantcreditrefunds) | **POST** /v2/pos/infogenesis/count/merchantCredit/refunds | Count refunded merchant credits |
| [**CountStaticVoucherRedemptions**](InfoGenesisReportsApi.md#countstaticvoucherredemptions) | **POST** /v2/pos/infogenesis/count/staticVoucher/redemptions | Count static voucher redemptions |
| [**CountStaticVoucherRefunds**](InfoGenesisReportsApi.md#countstaticvoucherrefunds) | **POST** /v2/pos/infogenesis/count/staticVoucher/refunds | Count static voucher refunds |
| [**FetchInfoGenesisAuthorizations**](InfoGenesisReportsApi.md#fetchinfogenesisauthorizations) | **POST** /v2/pos/infogenesis/authorizations | Get authorizations |
| [**FetchInfoGenesisCampaignData**](InfoGenesisReportsApi.md#fetchinfogenesiscampaigndata) | **POST** /v2/pos/infogenesis/campaign | Get campaign information |
| [**FetchInfoGenesisLookupRequests**](InfoGenesisReportsApi.md#fetchinfogenesislookuprequests) | **POST** /v2/pos/infogenesis/requests/lookup | Get lookup requests |
| [**FetchInfoGenesisLookupRequestsErrors**](InfoGenesisReportsApi.md#fetchinfogenesislookuprequestserrors) | **POST** /v2/pos/infogenesis/requests/lookup/errors | Get lookup request errors |
| [**FetchInfoGenesisRedeemedStaticVouchers**](InfoGenesisReportsApi.md#fetchinfogenesisredeemedstaticvouchers) | **POST** /v2/pos/infogenesis/staticVouchers/redeemed | Get redeemed static vouchers |
| [**FetchInfoGenesisRedeemedUniquePostingIDs**](InfoGenesisReportsApi.md#fetchinfogenesisredeemeduniquepostingids) | **GET** /v2/pos/infogenesis/postingIDs/redeemed | Get redeemed unique posting IDs |
| [**FetchInfoGenesisRedemptions**](InfoGenesisReportsApi.md#fetchinfogenesisredemptions) | **POST** /v2/pos/infogenesis/redemptions | Get redemptions |
| [**FetchInfoGenesisRefundedRoutingIDs**](InfoGenesisReportsApi.md#fetchinfogenesisrefundedroutingids) | **POST** /v2/pos/infogenesis/routingIDs/refunded | Get refunded unique posting IDs |
| [**FetchInfoGenesisRefundedStaticVouchers**](InfoGenesisReportsApi.md#fetchinfogenesisrefundedstaticvouchers) | **POST** /v2/pos/infogenesis/staticVouchers/refunded | Get refunded static vouchers |
| [**FetchInfoGenesisRefunds**](InfoGenesisReportsApi.md#fetchinfogenesisrefunds) | **POST** /v2/pos/infogenesis/refunds | Get refunds |
| [**FetchInfoGenesisRequest**](InfoGenesisReportsApi.md#fetchinfogenesisrequest) | **GET** /v2/pos/infogenesis/request/{transactionID} | Get request |
| [**FetchInfoGenesisRequests**](InfoGenesisReportsApi.md#fetchinfogenesisrequests) | **POST** /v2/pos/infogenesis/requests | Get requests |
| [**FetchInfoGenesisResponseErrors**](InfoGenesisReportsApi.md#fetchinfogenesisresponseerrors) | **GET** /v2/pos/infogenesis/responses/errors | Get response errors |
| [**FetchInfoGenesisResponses**](InfoGenesisReportsApi.md#fetchinfogenesisresponses) | **POST** /v2/pos/infogenesis/responses | Get responses |
| [**FetchInfoGenesisTransactionsWithUniquePostingIDs**](InfoGenesisReportsApi.md#fetchinfogenesistransactionswithuniquepostingids) | **POST** /v2/pos/infogenesis/transactions | Get transactions |

<a id="countadcreditsredemptions"></a>
# **CountAdCreditsRedemptions**
> WTCountResult CountAdCreditsRedemptions (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count redeemed ad credits

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
    public class CountAdCreditsRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count redeemed ad credits
                WTCountResult result = apiInstance.CountAdCreditsRedemptions(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountAdCreditsRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountAdCreditsRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redeemed ad credits
    ApiResponse<WTCountResult> response = apiInstance.CountAdCreditsRedemptionsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountAdCreditsRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countadcreditsrefunds"></a>
# **CountAdCreditsRefunds**
> WTCountResult CountAdCreditsRefunds (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count refunded ad credits

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
    public class CountAdCreditsRefundsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count refunded ad credits
                WTCountResult result = apiInstance.CountAdCreditsRefunds(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountAdCreditsRefunds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountAdCreditsRefundsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunded ad credits
    ApiResponse<WTCountResult> response = apiInstance.CountAdCreditsRefundsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountAdCreditsRefundsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countdynamicvoucherredemptions"></a>
# **CountDynamicVoucherRedemptions**
> WTCountResult CountDynamicVoucherRedemptions (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count dynamic voucher redemptions

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
    public class CountDynamicVoucherRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count dynamic voucher redemptions
                WTCountResult result = apiInstance.CountDynamicVoucherRedemptions(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountDynamicVoucherRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountDynamicVoucherRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count dynamic voucher redemptions
    ApiResponse<WTCountResult> response = apiInstance.CountDynamicVoucherRedemptionsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountDynamicVoucherRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countdynamicvoucherrefunds"></a>
# **CountDynamicVoucherRefunds**
> WTCountResult CountDynamicVoucherRefunds (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count dynamic voucher refunds

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
    public class CountDynamicVoucherRefundsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count dynamic voucher refunds
                WTCountResult result = apiInstance.CountDynamicVoucherRefunds(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountDynamicVoucherRefunds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountDynamicVoucherRefundsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count dynamic voucher refunds
    ApiResponse<WTCountResult> response = apiInstance.CountDynamicVoucherRefundsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountDynamicVoucherRefundsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countmembershippointsredemptions"></a>
# **CountMembershipPointsRedemptions**
> WTCountResult CountMembershipPointsRedemptions (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count redeemed membership points

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
    public class CountMembershipPointsRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count redeemed membership points
                WTCountResult result = apiInstance.CountMembershipPointsRedemptions(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountMembershipPointsRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountMembershipPointsRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redeemed membership points
    ApiResponse<WTCountResult> response = apiInstance.CountMembershipPointsRedemptionsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountMembershipPointsRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countmembershippointsrefunds"></a>
# **CountMembershipPointsRefunds**
> WTCountResult CountMembershipPointsRefunds (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count refunded membership points

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
    public class CountMembershipPointsRefundsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count refunded membership points
                WTCountResult result = apiInstance.CountMembershipPointsRefunds(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountMembershipPointsRefunds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountMembershipPointsRefundsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunded membership points
    ApiResponse<WTCountResult> response = apiInstance.CountMembershipPointsRefundsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountMembershipPointsRefundsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countmembershiptierredemptions"></a>
# **CountMembershipTierRedemptions**
> WTCountResult CountMembershipTierRedemptions (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count tier redemptions

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
    public class CountMembershipTierRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count tier redemptions
                WTCountResult result = apiInstance.CountMembershipTierRedemptions(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountMembershipTierRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountMembershipTierRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count tier redemptions
    ApiResponse<WTCountResult> response = apiInstance.CountMembershipTierRedemptionsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountMembershipTierRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countmembershiptierrefunds"></a>
# **CountMembershipTierRefunds**
> WTCountResult CountMembershipTierRefunds (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count tier refunds

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
    public class CountMembershipTierRefundsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count tier refunds
                WTCountResult result = apiInstance.CountMembershipTierRefunds(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountMembershipTierRefunds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountMembershipTierRefundsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count tier refunds
    ApiResponse<WTCountResult> response = apiInstance.CountMembershipTierRefundsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountMembershipTierRefundsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countmerchantcreditredemptions"></a>
# **CountMerchantCreditRedemptions**
> WTCountResult CountMerchantCreditRedemptions (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count redeemed merchant credits

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
    public class CountMerchantCreditRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count redeemed merchant credits
                WTCountResult result = apiInstance.CountMerchantCreditRedemptions(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountMerchantCreditRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountMerchantCreditRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count redeemed merchant credits
    ApiResponse<WTCountResult> response = apiInstance.CountMerchantCreditRedemptionsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountMerchantCreditRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countmerchantcreditrefunds"></a>
# **CountMerchantCreditRefunds**
> WTCountResult CountMerchantCreditRefunds (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count refunded merchant credits

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
    public class CountMerchantCreditRefundsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count refunded merchant credits
                WTCountResult result = apiInstance.CountMerchantCreditRefunds(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountMerchantCreditRefunds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountMerchantCreditRefundsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count refunded merchant credits
    ApiResponse<WTCountResult> response = apiInstance.CountMerchantCreditRefundsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountMerchantCreditRefundsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countstaticvoucherredemptions"></a>
# **CountStaticVoucherRedemptions**
> WTCountResult CountStaticVoucherRedemptions (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count static voucher redemptions

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
    public class CountStaticVoucherRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count static voucher redemptions
                WTCountResult result = apiInstance.CountStaticVoucherRedemptions(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountStaticVoucherRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountStaticVoucherRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count static voucher redemptions
    ApiResponse<WTCountResult> response = apiInstance.CountStaticVoucherRedemptionsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountStaticVoucherRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="countstaticvoucherrefunds"></a>
# **CountStaticVoucherRefunds**
> WTCountResult CountStaticVoucherRefunds (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Count static voucher refunds

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
    public class CountStaticVoucherRefundsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Count static voucher refunds
                WTCountResult result = apiInstance.CountStaticVoucherRefunds(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.CountStaticVoucherRefunds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountStaticVoucherRefundsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count static voucher refunds
    ApiResponse<WTCountResult> response = apiInstance.CountStaticVoucherRefundsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.CountStaticVoucherRefundsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="fetchinfogenesisauthorizations"></a>
# **FetchInfoGenesisAuthorizations**
> List&lt;Request&gt; FetchInfoGenesisAuthorizations (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Get authorizations

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
    public class FetchInfoGenesisAuthorizationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Get authorizations
                List<Request> result = apiInstance.FetchInfoGenesisAuthorizations(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisAuthorizations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisAuthorizationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get authorizations
    ApiResponse<List<Request>> response = apiInstance.FetchInfoGenesisAuthorizationsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisAuthorizationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**List&lt;Request&gt;**](Request.md)

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

<a id="fetchinfogenesiscampaigndata"></a>
# **FetchInfoGenesisCampaignData**
> bool FetchInfoGenesisCampaignData (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Get campaign information

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
    public class FetchInfoGenesisCampaignDataExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Get campaign information
                bool result = apiInstance.FetchInfoGenesisCampaignData(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisCampaignData: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisCampaignDataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get campaign information
    ApiResponse<bool> response = apiInstance.FetchInfoGenesisCampaignDataWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisCampaignDataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

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

<a id="fetchinfogenesislookuprequests"></a>
# **FetchInfoGenesisLookupRequests**
> List&lt;Request&gt; FetchInfoGenesisLookupRequests (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Get lookup requests

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
    public class FetchInfoGenesisLookupRequestsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Get lookup requests
                List<Request> result = apiInstance.FetchInfoGenesisLookupRequests(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisLookupRequests: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisLookupRequestsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get lookup requests
    ApiResponse<List<Request>> response = apiInstance.FetchInfoGenesisLookupRequestsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisLookupRequestsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**List&lt;Request&gt;**](Request.md)

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

<a id="fetchinfogenesislookuprequestserrors"></a>
# **FetchInfoGenesisLookupRequestsErrors**
> List&lt;Request&gt; FetchInfoGenesisLookupRequestsErrors (WTInfoGenesisLookupRequestErrors wTInfoGenesisLookupRequestErrors)

Get lookup request errors

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
    public class FetchInfoGenesisLookupRequestsErrorsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisLookupRequestErrors = new WTInfoGenesisLookupRequestErrors(); // WTInfoGenesisLookupRequestErrors | 

            try
            {
                // Get lookup request errors
                List<Request> result = apiInstance.FetchInfoGenesisLookupRequestsErrors(wTInfoGenesisLookupRequestErrors);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisLookupRequestsErrors: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisLookupRequestsErrorsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get lookup request errors
    ApiResponse<List<Request>> response = apiInstance.FetchInfoGenesisLookupRequestsErrorsWithHttpInfo(wTInfoGenesisLookupRequestErrors);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisLookupRequestsErrorsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisLookupRequestErrors** | [**WTInfoGenesisLookupRequestErrors**](WTInfoGenesisLookupRequestErrors.md) |  |  |

### Return type

[**List&lt;Request&gt;**](Request.md)

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

<a id="fetchinfogenesisredeemedstaticvouchers"></a>
# **FetchInfoGenesisRedeemedStaticVouchers**
> List&lt;StaticVoucher&gt; FetchInfoGenesisRedeemedStaticVouchers (WTInfoGenesisUniquePostingIDs wTInfoGenesisUniquePostingIDs)

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
    public class FetchInfoGenesisRedeemedStaticVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisUniquePostingIDs = new WTInfoGenesisUniquePostingIDs(); // WTInfoGenesisUniquePostingIDs | 

            try
            {
                // Get redeemed static vouchers
                List<StaticVoucher> result = apiInstance.FetchInfoGenesisRedeemedStaticVouchers(wTInfoGenesisUniquePostingIDs);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRedeemedStaticVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisRedeemedStaticVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redeemed static vouchers
    ApiResponse<List<StaticVoucher>> response = apiInstance.FetchInfoGenesisRedeemedStaticVouchersWithHttpInfo(wTInfoGenesisUniquePostingIDs);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRedeemedStaticVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisUniquePostingIDs** | [**WTInfoGenesisUniquePostingIDs**](WTInfoGenesisUniquePostingIDs.md) |  |  |

### Return type

[**List&lt;StaticVoucher&gt;**](StaticVoucher.md)

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

<a id="fetchinfogenesisredeemeduniquepostingids"></a>
# **FetchInfoGenesisRedeemedUniquePostingIDs**
> List&lt;Object&gt; FetchInfoGenesisRedeemedUniquePostingIDs (DateTime startDateTime, DateTime endDateTime)

Get redeemed unique posting IDs

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
    public class FetchInfoGenesisRedeemedUniquePostingIDsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get redeemed unique posting IDs
                List<Object> result = apiInstance.FetchInfoGenesisRedeemedUniquePostingIDs(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRedeemedUniquePostingIDs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisRedeemedUniquePostingIDsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redeemed unique posting IDs
    ApiResponse<List<Object>> response = apiInstance.FetchInfoGenesisRedeemedUniquePostingIDsWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRedeemedUniquePostingIDsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

### Return type

**List<Object>**

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

<a id="fetchinfogenesisredemptions"></a>
# **FetchInfoGenesisRedemptions**
> List&lt;Request&gt; FetchInfoGenesisRedemptions (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Get redemptions

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
    public class FetchInfoGenesisRedemptionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Get redemptions
                List<Request> result = apiInstance.FetchInfoGenesisRedemptions(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRedemptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisRedemptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get redemptions
    ApiResponse<List<Request>> response = apiInstance.FetchInfoGenesisRedemptionsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRedemptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**List&lt;Request&gt;**](Request.md)

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

<a id="fetchinfogenesisrefundedroutingids"></a>
# **FetchInfoGenesisRefundedRoutingIDs**
> List&lt;Object&gt; FetchInfoGenesisRefundedRoutingIDs (DateTime startDateTime, DateTime endDateTime)

Get refunded unique posting IDs

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
    public class FetchInfoGenesisRefundedRoutingIDsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get refunded unique posting IDs
                List<Object> result = apiInstance.FetchInfoGenesisRefundedRoutingIDs(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRefundedRoutingIDs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisRefundedRoutingIDsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refunded unique posting IDs
    ApiResponse<List<Object>> response = apiInstance.FetchInfoGenesisRefundedRoutingIDsWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRefundedRoutingIDsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

### Return type

**List<Object>**

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

<a id="fetchinfogenesisrefundedstaticvouchers"></a>
# **FetchInfoGenesisRefundedStaticVouchers**
> List&lt;StaticVoucher&gt; FetchInfoGenesisRefundedStaticVouchers (WTInfoGenesisRoutingIDs wTInfoGenesisRoutingIDs)

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
    public class FetchInfoGenesisRefundedStaticVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRoutingIDs = new WTInfoGenesisRoutingIDs(); // WTInfoGenesisRoutingIDs | 

            try
            {
                // Get refunded static vouchers
                List<StaticVoucher> result = apiInstance.FetchInfoGenesisRefundedStaticVouchers(wTInfoGenesisRoutingIDs);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRefundedStaticVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisRefundedStaticVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refunded static vouchers
    ApiResponse<List<StaticVoucher>> response = apiInstance.FetchInfoGenesisRefundedStaticVouchersWithHttpInfo(wTInfoGenesisRoutingIDs);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRefundedStaticVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRoutingIDs** | [**WTInfoGenesisRoutingIDs**](WTInfoGenesisRoutingIDs.md) |  |  |

### Return type

[**List&lt;StaticVoucher&gt;**](StaticVoucher.md)

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

<a id="fetchinfogenesisrefunds"></a>
# **FetchInfoGenesisRefunds**
> List&lt;Request&gt; FetchInfoGenesisRefunds (WTInfoGenesisRecordFilterParameters wTInfoGenesisRecordFilterParameters)

Get refunds

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
    public class FetchInfoGenesisRefundsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRecordFilterParameters = new WTInfoGenesisRecordFilterParameters(); // WTInfoGenesisRecordFilterParameters | 

            try
            {
                // Get refunds
                List<Request> result = apiInstance.FetchInfoGenesisRefunds(wTInfoGenesisRecordFilterParameters);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRefunds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisRefundsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get refunds
    ApiResponse<List<Request>> response = apiInstance.FetchInfoGenesisRefundsWithHttpInfo(wTInfoGenesisRecordFilterParameters);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRefundsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRecordFilterParameters** | [**WTInfoGenesisRecordFilterParameters**](WTInfoGenesisRecordFilterParameters.md) |  |  |

### Return type

[**List&lt;Request&gt;**](Request.md)

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

<a id="fetchinfogenesisrequest"></a>
# **FetchInfoGenesisRequest**
> Request FetchInfoGenesisRequest (string transactionID)

Get request

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
    public class FetchInfoGenesisRequestExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var transactionID = "transactionID_example";  // string | 

            try
            {
                // Get request
                Request result = apiInstance.FetchInfoGenesisRequest(transactionID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRequest: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisRequestWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get request
    ApiResponse<Request> response = apiInstance.FetchInfoGenesisRequestWithHttpInfo(transactionID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRequestWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **transactionID** | **string** |  |  |

### Return type

[**Request**](Request.md)

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

<a id="fetchinfogenesisrequests"></a>
# **FetchInfoGenesisRequests**
> List&lt;Request&gt; FetchInfoGenesisRequests (WTInfoGenesisRoutingIDs wTInfoGenesisRoutingIDs)

Get requests

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
    public class FetchInfoGenesisRequestsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRoutingIDs = new WTInfoGenesisRoutingIDs(); // WTInfoGenesisRoutingIDs | 

            try
            {
                // Get requests
                List<Request> result = apiInstance.FetchInfoGenesisRequests(wTInfoGenesisRoutingIDs);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRequests: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisRequestsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get requests
    ApiResponse<List<Request>> response = apiInstance.FetchInfoGenesisRequestsWithHttpInfo(wTInfoGenesisRoutingIDs);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisRequestsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRoutingIDs** | [**WTInfoGenesisRoutingIDs**](WTInfoGenesisRoutingIDs.md) |  |  |

### Return type

[**List&lt;Request&gt;**](Request.md)

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

<a id="fetchinfogenesisresponseerrors"></a>
# **FetchInfoGenesisResponseErrors**
> List&lt;Response&gt; FetchInfoGenesisResponseErrors (DateTime startDateTime, DateTime endDateTime)

Get response errors

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
    public class FetchInfoGenesisResponseErrorsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 

            try
            {
                // Get response errors
                List<Response> result = apiInstance.FetchInfoGenesisResponseErrors(startDateTime, endDateTime);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisResponseErrors: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisResponseErrorsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get response errors
    ApiResponse<List<Response>> response = apiInstance.FetchInfoGenesisResponseErrorsWithHttpInfo(startDateTime, endDateTime);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisResponseErrorsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |

### Return type

[**List&lt;Response&gt;**](Response.md)

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

<a id="fetchinfogenesisresponses"></a>
# **FetchInfoGenesisResponses**
> List&lt;Response&gt; FetchInfoGenesisResponses (WTInfoGenesisRoutingIDs wTInfoGenesisRoutingIDs)

Get responses

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
    public class FetchInfoGenesisResponsesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisRoutingIDs = new WTInfoGenesisRoutingIDs(); // WTInfoGenesisRoutingIDs | 

            try
            {
                // Get responses
                List<Response> result = apiInstance.FetchInfoGenesisResponses(wTInfoGenesisRoutingIDs);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisResponses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisResponsesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get responses
    ApiResponse<List<Response>> response = apiInstance.FetchInfoGenesisResponsesWithHttpInfo(wTInfoGenesisRoutingIDs);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisResponsesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisRoutingIDs** | [**WTInfoGenesisRoutingIDs**](WTInfoGenesisRoutingIDs.md) |  |  |

### Return type

[**List&lt;Response&gt;**](Response.md)

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

<a id="fetchinfogenesistransactionswithuniquepostingids"></a>
# **FetchInfoGenesisTransactionsWithUniquePostingIDs**
> List&lt;Request&gt; FetchInfoGenesisTransactionsWithUniquePostingIDs (WTInfoGenesisUniquePostingIDs wTInfoGenesisUniquePostingIDs)

Get transactions

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
    public class FetchInfoGenesisTransactionsWithUniquePostingIDsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new InfoGenesisReportsApi(httpClient, config, httpClientHandler);
            var wTInfoGenesisUniquePostingIDs = new WTInfoGenesisUniquePostingIDs(); // WTInfoGenesisUniquePostingIDs | 

            try
            {
                // Get transactions
                List<Request> result = apiInstance.FetchInfoGenesisTransactionsWithUniquePostingIDs(wTInfoGenesisUniquePostingIDs);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisTransactionsWithUniquePostingIDs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchInfoGenesisTransactionsWithUniquePostingIDsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get transactions
    ApiResponse<List<Request>> response = apiInstance.FetchInfoGenesisTransactionsWithUniquePostingIDsWithHttpInfo(wTInfoGenesisUniquePostingIDs);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InfoGenesisReportsApi.FetchInfoGenesisTransactionsWithUniquePostingIDsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTInfoGenesisUniquePostingIDs** | [**WTInfoGenesisUniquePostingIDs**](WTInfoGenesisUniquePostingIDs.md) |  |  |

### Return type

[**List&lt;Request&gt;**](Request.md)

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

