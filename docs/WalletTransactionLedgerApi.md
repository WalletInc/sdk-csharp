# WalletInc.Api.WalletTransactionLedgerApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchAllLedgerTransactions**](WalletTransactionLedgerApi.md#fetchallledgertransactions) | **GET** /v2/pos/ledger/transactions/all | Get ledger entries |

<a id="fetchallledgertransactions"></a>
# **FetchAllLedgerTransactions**
> FetchAllLedgerTransactions200Response FetchAllLedgerTransactions (DateTime startDateTime, DateTime endDateTime, double pageNum, double pageSize, ApplicableTerminals? registerType = null)

Get ledger entries

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
    public class FetchAllLedgerTransactionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new WalletTransactionLedgerApi(httpClient, config, httpClientHandler);
            var startDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var endDateTime = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime | 
            var pageNum = 1.2D;  // double | 
            var pageSize = 1.2D;  // double | 
            var registerType = new ApplicableTerminals?(); // ApplicableTerminals? |  (optional) 

            try
            {
                // Get ledger entries
                FetchAllLedgerTransactions200Response result = apiInstance.FetchAllLedgerTransactions(startDateTime, endDateTime, pageNum, pageSize, registerType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalletTransactionLedgerApi.FetchAllLedgerTransactions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllLedgerTransactionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get ledger entries
    ApiResponse<FetchAllLedgerTransactions200Response> response = apiInstance.FetchAllLedgerTransactionsWithHttpInfo(startDateTime, endDateTime, pageNum, pageSize, registerType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalletTransactionLedgerApi.FetchAllLedgerTransactionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **startDateTime** | **DateTime** |  |  |
| **endDateTime** | **DateTime** |  |  |
| **pageNum** | **double** |  |  |
| **pageSize** | **double** |  |  |
| **registerType** | [**ApplicableTerminals?**](ApplicableTerminals?.md) |  | [optional]  |

### Return type

[**FetchAllLedgerTransactions200Response**](FetchAllLedgerTransactions200Response.md)

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

