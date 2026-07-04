# WalletInc.Api.ImportedListsApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveRecipient**](ImportedListsApi.md#archiverecipient) | **DELETE** /v2/sms/importedList/recipients/{id} | Archive recipient |
| [**CountImportedListRecipients**](ImportedListsApi.md#countimportedlistrecipients) | **GET** /v2/sms/importedList/recipients/count/{listID} | Count imported list recipients |
| [**CreateImportedList**](ImportedListsApi.md#createimportedlist) | **POST** /v2/sms/importedList | Create imported list |
| [**CreateRecipientInImportedList**](ImportedListsApi.md#createrecipientinimportedlist) | **POST** /v2/sms/importedList/recipients/create | Add new recipient in an imported list |
| [**ExportImportedListRecipients**](ImportedListsApi.md#exportimportedlistrecipients) | **POST** /v2/sms/importedList/recipients/export/{importedListID} | Export imported list recipients |
| [**FetchImportedList**](ImportedListsApi.md#fetchimportedlist) | **GET** /v2/merchant/lists/imported/{listID} | Get imported list |
| [**FetchImportedListRecipients**](ImportedListsApi.md#fetchimportedlistrecipients) | **GET** /v2/sms/importedList/recipients/{listID} | Get imported list recipients |
| [**FetchImportedListRecipientsByPage**](ImportedListsApi.md#fetchimportedlistrecipientsbypage) | **GET** /v2/sms/importedList/recipients/page/{listID} | Get imported list recipients by page |
| [**FetchImportedLists**](ImportedListsApi.md#fetchimportedlists) | **GET** /v2/merchant/lists/imported/all | Get all imported lists |
| [**ImportImportedListRecipients**](ImportedListsApi.md#importimportedlistrecipients) | **POST** /v2/sms/importedList/recipients/import/{importedListID} | Import imported list recipients |
| [**ImportImportedListRecipientsFromMembershipTier**](ImportedListsApi.md#importimportedlistrecipientsfrommembershiptier) | **POST** /v2/sms/importedList/recipients/import-from-tier | Import imported list recipients from a given membership tier |
| [**RestoreRecipient**](ImportedListsApi.md#restorerecipient) | **PATCH** /v2/sms/importedList/recipients/{id} | Restore recipient |
| [**SaveImportedList**](ImportedListsApi.md#saveimportedlist) | **PUT** /v2/sms/importedList/{listID} | Save imported list |

<a id="archiverecipient"></a>
# **ArchiveRecipient**
> ImportedListRecipient ArchiveRecipient (string id)

Archive recipient

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
    public class ArchiveRecipientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Archive recipient
                ImportedListRecipient result = apiInstance.ArchiveRecipient(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.ArchiveRecipient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveRecipientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive recipient
    ApiResponse<ImportedListRecipient> response = apiInstance.ArchiveRecipientWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.ArchiveRecipientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**ImportedListRecipient**](ImportedListRecipient.md)

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

<a id="countimportedlistrecipients"></a>
# **CountImportedListRecipients**
> WTCountResult CountImportedListRecipients (string listID, bool? isArchiveIncluded = null, DateTime? startDate = null, DateTime? endDate = null)

Count imported list recipients

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
    public class CountImportedListRecipientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var isArchiveIncluded = true;  // bool? |  (optional) 
            var startDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 
            var endDate = DateTime.Parse("2013-10-20T19:20:30+01:00");  // DateTime? |  (optional) 

            try
            {
                // Count imported list recipients
                WTCountResult result = apiInstance.CountImportedListRecipients(listID, isArchiveIncluded, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.CountImportedListRecipients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CountImportedListRecipientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Count imported list recipients
    ApiResponse<WTCountResult> response = apiInstance.CountImportedListRecipientsWithHttpInfo(listID, isArchiveIncluded, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.CountImportedListRecipientsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |
| **startDate** | **DateTime?** |  | [optional]  |
| **endDate** | **DateTime?** |  | [optional]  |

### Return type

[**WTCountResult**](WTCountResult.md)

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

<a id="createimportedlist"></a>
# **CreateImportedList**
> ImportedList CreateImportedList (WTSMSImportedListCreate wTSMSImportedListCreate)

Create imported list

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
    public class CreateImportedListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var wTSMSImportedListCreate = new WTSMSImportedListCreate(); // WTSMSImportedListCreate | 

            try
            {
                // Create imported list
                ImportedList result = apiInstance.CreateImportedList(wTSMSImportedListCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.CreateImportedList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateImportedListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create imported list
    ApiResponse<ImportedList> response = apiInstance.CreateImportedListWithHttpInfo(wTSMSImportedListCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.CreateImportedListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTSMSImportedListCreate** | [**WTSMSImportedListCreate**](WTSMSImportedListCreate.md) |  |  |

### Return type

[**ImportedList**](ImportedList.md)

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

<a id="createrecipientinimportedlist"></a>
# **CreateRecipientInImportedList**
> ImportedListRecipient CreateRecipientInImportedList (SSImportedListRecipientCreateParams sSImportedListRecipientCreateParams)

Add new recipient in an imported list

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
    public class CreateRecipientInImportedListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var sSImportedListRecipientCreateParams = new SSImportedListRecipientCreateParams(); // SSImportedListRecipientCreateParams | 

            try
            {
                // Add new recipient in an imported list
                ImportedListRecipient result = apiInstance.CreateRecipientInImportedList(sSImportedListRecipientCreateParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.CreateRecipientInImportedList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateRecipientInImportedListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add new recipient in an imported list
    ApiResponse<ImportedListRecipient> response = apiInstance.CreateRecipientInImportedListWithHttpInfo(sSImportedListRecipientCreateParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.CreateRecipientInImportedListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sSImportedListRecipientCreateParams** | [**SSImportedListRecipientCreateParams**](SSImportedListRecipientCreateParams.md) |  |  |

### Return type

[**ImportedListRecipient**](ImportedListRecipient.md)

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

<a id="exportimportedlistrecipients"></a>
# **ExportImportedListRecipients**
> string ExportImportedListRecipients (string importedListID)

Export imported list recipients

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
    public class ExportImportedListRecipientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var importedListID = "importedListID_example";  // string | 

            try
            {
                // Export imported list recipients
                string result = apiInstance.ExportImportedListRecipients(importedListID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.ExportImportedListRecipients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportImportedListRecipientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export imported list recipients
    ApiResponse<string> response = apiInstance.ExportImportedListRecipientsWithHttpInfo(importedListID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.ExportImportedListRecipientsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **importedListID** | **string** |  |  |

### Return type

**string**

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

<a id="fetchimportedlist"></a>
# **FetchImportedList**
> ImportedList FetchImportedList (string listID)

Get imported list

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
    public class FetchImportedListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 

            try
            {
                // Get imported list
                ImportedList result = apiInstance.FetchImportedList(listID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.FetchImportedList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchImportedListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get imported list
    ApiResponse<ImportedList> response = apiInstance.FetchImportedListWithHttpInfo(listID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.FetchImportedListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |

### Return type

[**ImportedList**](ImportedList.md)

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

<a id="fetchimportedlistrecipients"></a>
# **FetchImportedListRecipients**
> List&lt;ImportedListRecipient&gt; FetchImportedListRecipients (string listID)

Get imported list recipients

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
    public class FetchImportedListRecipientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 

            try
            {
                // Get imported list recipients
                List<ImportedListRecipient> result = apiInstance.FetchImportedListRecipients(listID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.FetchImportedListRecipients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchImportedListRecipientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get imported list recipients
    ApiResponse<List<ImportedListRecipient>> response = apiInstance.FetchImportedListRecipientsWithHttpInfo(listID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.FetchImportedListRecipientsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |

### Return type

[**List&lt;ImportedListRecipient&gt;**](ImportedListRecipient.md)

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

<a id="fetchimportedlistrecipientsbypage"></a>
# **FetchImportedListRecipientsByPage**
> FetchImportedListRecipientsByPage200Response FetchImportedListRecipientsByPage (string listID, double? pageSize = null, double? pageNum = null, bool? isArchiveIncluded = null)

Get imported list recipients by page

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
    public class FetchImportedListRecipientsByPageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var pageSize = 1.2D;  // double? |  (optional) 
            var pageNum = 1.2D;  // double? |  (optional) 
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get imported list recipients by page
                FetchImportedListRecipientsByPage200Response result = apiInstance.FetchImportedListRecipientsByPage(listID, pageSize, pageNum, isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.FetchImportedListRecipientsByPage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchImportedListRecipientsByPageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get imported list recipients by page
    ApiResponse<FetchImportedListRecipientsByPage200Response> response = apiInstance.FetchImportedListRecipientsByPageWithHttpInfo(listID, pageSize, pageNum, isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.FetchImportedListRecipientsByPageWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **pageSize** | **double?** |  | [optional]  |
| **pageNum** | **double?** |  | [optional]  |
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**FetchImportedListRecipientsByPage200Response**](FetchImportedListRecipientsByPage200Response.md)

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

<a id="fetchimportedlists"></a>
# **FetchImportedLists**
> Object FetchImportedLists (bool? isArchiveIncluded = null)

Get all imported lists

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
    public class FetchImportedListsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all imported lists
                Object result = apiInstance.FetchImportedLists(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.FetchImportedLists: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchImportedListsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all imported lists
    ApiResponse<Object> response = apiInstance.FetchImportedListsWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.FetchImportedListsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

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

<a id="importimportedlistrecipients"></a>
# **ImportImportedListRecipients**
> string ImportImportedListRecipients (string importedListID, WTEmployeeImportRecords wTEmployeeImportRecords)

Import imported list recipients

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
    public class ImportImportedListRecipientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var importedListID = "importedListID_example";  // string | 
            var wTEmployeeImportRecords = new WTEmployeeImportRecords(); // WTEmployeeImportRecords | 

            try
            {
                // Import imported list recipients
                string result = apiInstance.ImportImportedListRecipients(importedListID, wTEmployeeImportRecords);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.ImportImportedListRecipients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImportImportedListRecipientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Import imported list recipients
    ApiResponse<string> response = apiInstance.ImportImportedListRecipientsWithHttpInfo(importedListID, wTEmployeeImportRecords);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.ImportImportedListRecipientsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **importedListID** | **string** |  |  |
| **wTEmployeeImportRecords** | [**WTEmployeeImportRecords**](WTEmployeeImportRecords.md) |  |  |

### Return type

**string**

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

<a id="importimportedlistrecipientsfrommembershiptier"></a>
# **ImportImportedListRecipientsFromMembershipTier**
> string ImportImportedListRecipientsFromMembershipTier (WTImportedListRecipientFromMembershipTierImport wTImportedListRecipientFromMembershipTierImport)

Import imported list recipients from a given membership tier

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
    public class ImportImportedListRecipientsFromMembershipTierExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var wTImportedListRecipientFromMembershipTierImport = new WTImportedListRecipientFromMembershipTierImport(); // WTImportedListRecipientFromMembershipTierImport | 

            try
            {
                // Import imported list recipients from a given membership tier
                string result = apiInstance.ImportImportedListRecipientsFromMembershipTier(wTImportedListRecipientFromMembershipTierImport);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.ImportImportedListRecipientsFromMembershipTier: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImportImportedListRecipientsFromMembershipTierWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Import imported list recipients from a given membership tier
    ApiResponse<string> response = apiInstance.ImportImportedListRecipientsFromMembershipTierWithHttpInfo(wTImportedListRecipientFromMembershipTierImport);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.ImportImportedListRecipientsFromMembershipTierWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTImportedListRecipientFromMembershipTierImport** | [**WTImportedListRecipientFromMembershipTierImport**](WTImportedListRecipientFromMembershipTierImport.md) |  |  |

### Return type

**string**

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

<a id="restorerecipient"></a>
# **RestoreRecipient**
> ImportedListRecipient RestoreRecipient (string id)

Restore recipient

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
    public class RestoreRecipientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var id = "id_example";  // string | 

            try
            {
                // Restore recipient
                ImportedListRecipient result = apiInstance.RestoreRecipient(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.RestoreRecipient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreRecipientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore recipient
    ApiResponse<ImportedListRecipient> response = apiInstance.RestoreRecipientWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.RestoreRecipientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

[**ImportedListRecipient**](ImportedListRecipient.md)

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

<a id="saveimportedlist"></a>
# **SaveImportedList**
> ImportedList SaveImportedList (string listID, WTSMSImportedListCreate wTSMSImportedListCreate)

Save imported list

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
    public class SaveImportedListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new ImportedListsApi(httpClient, config, httpClientHandler);
            var listID = "listID_example";  // string | 
            var wTSMSImportedListCreate = new WTSMSImportedListCreate(); // WTSMSImportedListCreate | 

            try
            {
                // Save imported list
                ImportedList result = apiInstance.SaveImportedList(listID, wTSMSImportedListCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportedListsApi.SaveImportedList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveImportedListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Save imported list
    ApiResponse<ImportedList> response = apiInstance.SaveImportedListWithHttpInfo(listID, wTSMSImportedListCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportedListsApi.SaveImportedListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listID** | **string** |  |  |
| **wTSMSImportedListCreate** | [**WTSMSImportedListCreate**](WTSMSImportedListCreate.md) |  |  |

### Return type

[**ImportedList**](ImportedList.md)

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

