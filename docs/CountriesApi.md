# WalletInc.Api.CountriesApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FetchAllCountries**](CountriesApi.md#fetchallcountries) | **GET** /system/countries/all | Get all Countries with ISO abbreviations &amp; Telephone country code prefixes |

<a id="fetchallcountries"></a>
# **FetchAllCountries**
> List&lt;FetchAllCountries200ResponseInner&gt; FetchAllCountries ()

Get all Countries with ISO abbreviations & Telephone country code prefixes

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
    public class FetchAllCountriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new CountriesApi(httpClient, config, httpClientHandler);

            try
            {
                // Get all Countries with ISO abbreviations & Telephone country code prefixes
                List<FetchAllCountries200ResponseInner> result = apiInstance.FetchAllCountries();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CountriesApi.FetchAllCountries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchAllCountriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Countries with ISO abbreviations & Telephone country code prefixes
    ApiResponse<List<FetchAllCountries200ResponseInner>> response = apiInstance.FetchAllCountriesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CountriesApi.FetchAllCountriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;FetchAllCountries200ResponseInner&gt;**](FetchAllCountries200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ok |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

