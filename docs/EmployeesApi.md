# WalletInc.Api.EmployeesApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddPeerToRoles**](EmployeesApi.md#addpeertoroles) | **POST** /v2/employee/roles/peer/{userID} | Add peer to roles |
| [**CreateDocument**](EmployeesApi.md#createdocument) | **POST** /v2/employee/document | Create document |
| [**CreateEmployeePeer**](EmployeesApi.md#createemployeepeer) | **POST** /v2/employee/peer | Create employee peer |
| [**CreateFile**](EmployeesApi.md#createfile) | **POST** /v2/employee/file/create | Create file |
| [**CreateMediaFile**](EmployeesApi.md#createmediafile) | **POST** /v2/employee/mediaFile | Create media file |
| [**DeleteDocument**](EmployeesApi.md#deletedocument) | **DELETE** /v2/employee/document/{documentID} | Delete document |
| [**DeleteMediaFile**](EmployeesApi.md#deletemediafile) | **DELETE** /v2/employee/mediaFile/{mediaFileID} | Delete media file |
| [**DownloadFile**](EmployeesApi.md#downloadfile) | **GET** /v2/employee/file/download/{fileID} | Get URL for file download |
| [**ExportClubMembers**](EmployeesApi.md#exportclubmembers) | **PUT** /v2/employee/export/members | Export club members |
| [**ExportMerchantCredits**](EmployeesApi.md#exportmerchantcredits) | **PUT** /v2/employee/export/merchantCredits | Export merchant credits |
| [**ExportStaticVoucherCampaign**](EmployeesApi.md#exportstaticvouchercampaign) | **PUT** /v2/employee/export/staticVoucherCampaign/{campaignID} | Export static voucher campaign |
| [**FailedImport**](EmployeesApi.md#failedimport) | **GET** /v2/employee/file/imports/failed/{fileID} | Get URL to download a failed import |
| [**FetchDocuments**](EmployeesApi.md#fetchdocuments) | **GET** /v2/employee/documents/all | Get all documents |
| [**FetchDynamicVouchers**](EmployeesApi.md#fetchdynamicvouchers) | **GET** /v2/employee/dynamicVouchers/all | Get all dynamic vouchers |
| [**FetchMediaFiles**](EmployeesApi.md#fetchmediafiles) | **GET** /v2/employee/mediaFiles/all | Get all media files |
| [**FetchMerchant**](EmployeesApi.md#fetchmerchant) | **GET** /v2/employee/merchant | Create employee alert |
| [**FetchMessages**](EmployeesApi.md#fetchmessages) | **GET** /v2/employee/messages/all | Get all messages |
| [**FetchOptInListSource**](EmployeesApi.md#fetchoptinlistsource) | **GET** /v2/employee/optInListSource/{sourceID} | Get opt in list source |
| [**FetchOptInListSourcesCreatedByEmployee**](EmployeesApi.md#fetchoptinlistsourcescreatedbyemployee) | **GET** /v2/employee/optInListSources/all | Get all opt in list sources |
| [**FetchPeerActivity**](EmployeesApi.md#fetchpeeractivity) | **GET** /v2/employee/peer/activity/{employeeID} | Get peer activity |
| [**FetchPeersPermissions**](EmployeesApi.md#fetchpeerspermissions) | **GET** /v2/employee/peer/permissions/{userID} | Get peer permissions |
| [**FetchProfileInfo**](EmployeesApi.md#fetchprofileinfo) | **GET** /v2/employee | Get employee info |
| [**ImportClubMembers**](EmployeesApi.md#importclubmembers) | **POST** /v2/employee/import/members | Import club members |
| [**ImportMerchantCredits**](EmployeesApi.md#importmerchantcredits) | **POST** /v2/employee/import/merchantCredits | Import merchant credits |
| [**LoadWebpagesOfEmployee**](EmployeesApi.md#loadwebpagesofemployee) | **GET** /v2/employee/webpages/all | Get employee&#39;s permissions |
| [**ModifyPeersRoles**](EmployeesApi.md#modifypeersroles) | **PUT** /v2/employee/peer/permissions/{userID} | Modify peer&#39;s roles |
| [**PresignFile**](EmployeesApi.md#presignfile) | **POST** /v2/employee/file/presign | Presign file for upload |
| [**RemovePeerFromAllRoles**](EmployeesApi.md#removepeerfromallroles) | **DELETE** /v2/employee/peer/permissions/{userID} | Remove peer from all roles |
| [**ScheduleAdvertisementCredit**](EmployeesApi.md#scheduleadvertisementcredit) | **POST** /v2/employee/sms/schedule/adCredit/{advertisementCreditID} | Schedule Ad Credit |
| [**ScheduleDynamicVoucher**](EmployeesApi.md#scheduledynamicvoucher) | **POST** /v2/employee/sms/schedule/dynamicVoucher/{dynamicVoucherID} | Schedule Dynamic Voucher to list |
| [**ScheduleDynamicVoucherToRecipient**](EmployeesApi.md#scheduledynamicvouchertorecipient) | **POST** /v2/employee/sms/schedule/recipient/dynamicVoucher/{dynamicVoucherID} | Schedule Dyanamic Voucher to recipient |
| [**ScheduleSimpleSMS**](EmployeesApi.md#schedulesimplesms) | **POST** /v2/employee/sms/schedule/simple | Schedule Simple SMS broadcast to list |
| [**ScheduleSimpleSMSToRecipient**](EmployeesApi.md#schedulesimplesmstorecipient) | **POST** /v2/employee/sms/schedule/recipient/simple | Schedule Simple SMS broadcast to recipient |
| [**SendHelpDeskResponse**](EmployeesApi.md#sendhelpdeskresponse) | **POST** /v2/employee/helpDesk/response | Send help desk response |
| [**SendSmsCampaignBroadcast**](EmployeesApi.md#sendsmscampaignbroadcast) | **POST** /v2/employee/sms/schedule/campaign/{staticVoucherCampaignID} | Schedule SMS Campaign Broadcast |
| [**SetAlertsRead**](EmployeesApi.md#setalertsread) | **PATCH** /v2/employee/alerts | Mark alerts as read |
| [**SetExportDataFilesRead**](EmployeesApi.md#setexportdatafilesread) | **PUT** /v2/employee/export/dataFiles | Mark export data files as read |
| [**SetHelpDeskRequestResolved**](EmployeesApi.md#sethelpdeskrequestresolved) | **PATCH** /v2/employee/helpDesk/request/{helpDeskRequestID} | Resolve help desk request |
| [**SetMessagesRead**](EmployeesApi.md#setmessagesread) | **PATCH** /v2/employee/messages | Mark messages as read |
| [**SetProfilePicture**](EmployeesApi.md#setprofilepicture) | **PUT** /v2/employee/profile/picture | Set profile picture |
| [**UpdateClubMembers**](EmployeesApi.md#updateclubmembers) | **PUT** /v2/employee/update/members | Update club members |
| [**UpdateEmailNotificationPreference**](EmployeesApi.md#updateemailnotificationpreference) | **PUT** /v2/employee/emailNotificationPreference | Changes the employee&#39;s email notification preference to enabled or disabled |
| [**UpdateEmployeePeer**](EmployeesApi.md#updateemployeepeer) | **PUT** /v2/employee/peer/{userID} | Update peer |

<a id="addpeertoroles"></a>
# **AddPeerToRoles**
> string AddPeerToRoles (string userID, WTEmployeePeerRoles wTEmployeePeerRoles)

Add peer to roles

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
    public class AddPeerToRolesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var userID = "userID_example";  // string | 
            var wTEmployeePeerRoles = new WTEmployeePeerRoles(); // WTEmployeePeerRoles | 

            try
            {
                // Add peer to roles
                string result = apiInstance.AddPeerToRoles(userID, wTEmployeePeerRoles);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.AddPeerToRoles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddPeerToRolesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add peer to roles
    ApiResponse<string> response = apiInstance.AddPeerToRolesWithHttpInfo(userID, wTEmployeePeerRoles);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.AddPeerToRolesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userID** | **string** |  |  |
| **wTEmployeePeerRoles** | [**WTEmployeePeerRoles**](WTEmployeePeerRoles.md) |  |  |

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

<a id="createdocument"></a>
# **CreateDocument**
> Document CreateDocument (WTEmployeeCreateDocument wTEmployeeCreateDocument)

Create document

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
    public class CreateDocumentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeCreateDocument = new WTEmployeeCreateDocument(); // WTEmployeeCreateDocument | 

            try
            {
                // Create document
                Document result = apiInstance.CreateDocument(wTEmployeeCreateDocument);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.CreateDocument: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDocumentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create document
    ApiResponse<Document> response = apiInstance.CreateDocumentWithHttpInfo(wTEmployeeCreateDocument);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.CreateDocumentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeCreateDocument** | [**WTEmployeeCreateDocument**](WTEmployeeCreateDocument.md) |  |  |

### Return type

[**Document**](Document.md)

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

<a id="createemployeepeer"></a>
# **CreateEmployeePeer**
> Employee CreateEmployeePeer (WTEmployeeCreate wTEmployeeCreate)

Create employee peer

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
    public class CreateEmployeePeerExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeCreate = new WTEmployeeCreate(); // WTEmployeeCreate | 

            try
            {
                // Create employee peer
                Employee result = apiInstance.CreateEmployeePeer(wTEmployeeCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.CreateEmployeePeer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEmployeePeerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create employee peer
    ApiResponse<Employee> response = apiInstance.CreateEmployeePeerWithHttpInfo(wTEmployeeCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.CreateEmployeePeerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeCreate** | [**WTEmployeeCreate**](WTEmployeeCreate.md) |  |  |

### Return type

[**Employee**](Employee.md)

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

<a id="createfile"></a>
# **CreateFile**
> CreateFile200Response CreateFile (WTEmployeeFileCreate wTEmployeeFileCreate)

Create file

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
    public class CreateFileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeFileCreate = new WTEmployeeFileCreate(); // WTEmployeeFileCreate | 

            try
            {
                // Create file
                CreateFile200Response result = apiInstance.CreateFile(wTEmployeeFileCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.CreateFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create file
    ApiResponse<CreateFile200Response> response = apiInstance.CreateFileWithHttpInfo(wTEmployeeFileCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.CreateFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeFileCreate** | [**WTEmployeeFileCreate**](WTEmployeeFileCreate.md) |  |  |

### Return type

[**CreateFile200Response**](CreateFile200Response.md)

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

<a id="createmediafile"></a>
# **CreateMediaFile**
> MediaFile CreateMediaFile (WTEmployeeCreateMediaFile wTEmployeeCreateMediaFile)

Create media file

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
    public class CreateMediaFileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeCreateMediaFile = new WTEmployeeCreateMediaFile(); // WTEmployeeCreateMediaFile | 

            try
            {
                // Create media file
                MediaFile result = apiInstance.CreateMediaFile(wTEmployeeCreateMediaFile);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.CreateMediaFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateMediaFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create media file
    ApiResponse<MediaFile> response = apiInstance.CreateMediaFileWithHttpInfo(wTEmployeeCreateMediaFile);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.CreateMediaFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeCreateMediaFile** | [**WTEmployeeCreateMediaFile**](WTEmployeeCreateMediaFile.md) |  |  |

### Return type

[**MediaFile**](MediaFile.md)

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

<a id="deletedocument"></a>
# **DeleteDocument**
> Document DeleteDocument (string documentID)

Delete document

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
    public class DeleteDocumentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var documentID = "documentID_example";  // string | 

            try
            {
                // Delete document
                Document result = apiInstance.DeleteDocument(documentID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.DeleteDocument: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDocumentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete document
    ApiResponse<Document> response = apiInstance.DeleteDocumentWithHttpInfo(documentID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.DeleteDocumentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentID** | **string** |  |  |

### Return type

[**Document**](Document.md)

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

<a id="deletemediafile"></a>
# **DeleteMediaFile**
> MediaFile DeleteMediaFile (string mediaFileID)

Delete media file

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
    public class DeleteMediaFileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var mediaFileID = "mediaFileID_example";  // string | 

            try
            {
                // Delete media file
                MediaFile result = apiInstance.DeleteMediaFile(mediaFileID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.DeleteMediaFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteMediaFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete media file
    ApiResponse<MediaFile> response = apiInstance.DeleteMediaFileWithHttpInfo(mediaFileID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.DeleteMediaFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **mediaFileID** | **string** |  |  |

### Return type

[**MediaFile**](MediaFile.md)

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

<a id="downloadfile"></a>
# **DownloadFile**
> string DownloadFile (string fileID)

Get URL for file download

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
    public class DownloadFileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var fileID = "fileID_example";  // string | 

            try
            {
                // Get URL for file download
                string result = apiInstance.DownloadFile(fileID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.DownloadFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get URL for file download
    ApiResponse<string> response = apiInstance.DownloadFileWithHttpInfo(fileID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.DownloadFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fileID** | **string** |  |  |

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

<a id="exportclubmembers"></a>
# **ExportClubMembers**
> string ExportClubMembers ()

Export club members

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
    public class ExportClubMembersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Export club members
                string result = apiInstance.ExportClubMembers();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ExportClubMembers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportClubMembersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export club members
    ApiResponse<string> response = apiInstance.ExportClubMembersWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ExportClubMembersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
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

<a id="exportmerchantcredits"></a>
# **ExportMerchantCredits**
> string ExportMerchantCredits ()

Export merchant credits

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
    public class ExportMerchantCreditsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Export merchant credits
                string result = apiInstance.ExportMerchantCredits();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ExportMerchantCredits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportMerchantCreditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export merchant credits
    ApiResponse<string> response = apiInstance.ExportMerchantCreditsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ExportMerchantCreditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
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

<a id="exportstaticvouchercampaign"></a>
# **ExportStaticVoucherCampaign**
> string ExportStaticVoucherCampaign (string campaignID)

Export static voucher campaign

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
    public class ExportStaticVoucherCampaignExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var campaignID = "campaignID_example";  // string | 

            try
            {
                // Export static voucher campaign
                string result = apiInstance.ExportStaticVoucherCampaign(campaignID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ExportStaticVoucherCampaign: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportStaticVoucherCampaignWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export static voucher campaign
    ApiResponse<string> response = apiInstance.ExportStaticVoucherCampaignWithHttpInfo(campaignID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ExportStaticVoucherCampaignWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **campaignID** | **string** |  |  |

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

<a id="failedimport"></a>
# **FailedImport**
> string FailedImport (string fileID)

Get URL to download a failed import

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
    public class FailedImportExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var fileID = "fileID_example";  // string | 

            try
            {
                // Get URL to download a failed import
                string result = apiInstance.FailedImport(fileID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FailedImport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FailedImportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get URL to download a failed import
    ApiResponse<string> response = apiInstance.FailedImportWithHttpInfo(fileID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FailedImportWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fileID** | **string** |  |  |

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

<a id="fetchdocuments"></a>
# **FetchDocuments**
> List&lt;Document&gt; FetchDocuments (string? folder = null)

Get all documents

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
    public class FetchDocumentsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var folder = "folder_example";  // string? |  (optional) 

            try
            {
                // Get all documents
                List<Document> result = apiInstance.FetchDocuments(folder);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchDocuments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDocumentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all documents
    ApiResponse<List<Document>> response = apiInstance.FetchDocumentsWithHttpInfo(folder);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchDocumentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **folder** | **string?** |  | [optional]  |

### Return type

[**List&lt;Document&gt;**](Document.md)

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

<a id="fetchdynamicvouchers"></a>
# **FetchDynamicVouchers**
> List&lt;DynamicVoucher&gt; FetchDynamicVouchers (bool? isArchiveIncluded = null)

Get all dynamic vouchers

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
    public class FetchDynamicVouchersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var isArchiveIncluded = true;  // bool? |  (optional) 

            try
            {
                // Get all dynamic vouchers
                List<DynamicVoucher> result = apiInstance.FetchDynamicVouchers(isArchiveIncluded);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchDynamicVouchers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchDynamicVouchersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all dynamic vouchers
    ApiResponse<List<DynamicVoucher>> response = apiInstance.FetchDynamicVouchersWithHttpInfo(isArchiveIncluded);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchDynamicVouchersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **isArchiveIncluded** | **bool?** |  | [optional]  |

### Return type

[**List&lt;DynamicVoucher&gt;**](DynamicVoucher.md)

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

<a id="fetchmediafiles"></a>
# **FetchMediaFiles**
> List&lt;MediaFile&gt; FetchMediaFiles (string? folder = null)

Get all media files

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
    public class FetchMediaFilesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var folder = "folder_example";  // string? |  (optional) 

            try
            {
                // Get all media files
                List<MediaFile> result = apiInstance.FetchMediaFiles(folder);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchMediaFiles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMediaFilesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all media files
    ApiResponse<List<MediaFile>> response = apiInstance.FetchMediaFilesWithHttpInfo(folder);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchMediaFilesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **folder** | **string?** |  | [optional]  |

### Return type

[**List&lt;MediaFile&gt;**](MediaFile.md)

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

<a id="fetchmerchant"></a>
# **FetchMerchant**
> Object FetchMerchant ()

Create employee alert

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
    public class FetchMerchantExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Create employee alert
                Object result = apiInstance.FetchMerchant();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchMerchant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMerchantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create employee alert
    ApiResponse<Object> response = apiInstance.FetchMerchantWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchMerchantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
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

<a id="fetchmessages"></a>
# **FetchMessages**
> List&lt;Message&gt; FetchMessages ()

Get all messages

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
    public class FetchMessagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Get all messages
                List<Message> result = apiInstance.FetchMessages();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all messages
    ApiResponse<List<Message>> response = apiInstance.FetchMessagesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchMessagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;Message&gt;**](Message.md)

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

<a id="fetchoptinlistsource"></a>
# **FetchOptInListSource**
> OptInListSource FetchOptInListSource (string sourceID)

Get opt in list source

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
    public class FetchOptInListSourceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var sourceID = "sourceID_example";  // string | 

            try
            {
                // Get opt in list source
                OptInListSource result = apiInstance.FetchOptInListSource(sourceID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchOptInListSource: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListSourceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get opt in list source
    ApiResponse<OptInListSource> response = apiInstance.FetchOptInListSourceWithHttpInfo(sourceID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchOptInListSourceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sourceID** | **string** |  |  |

### Return type

[**OptInListSource**](OptInListSource.md)

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

<a id="fetchoptinlistsourcescreatedbyemployee"></a>
# **FetchOptInListSourcesCreatedByEmployee**
> List&lt;OptInListSource&gt; FetchOptInListSourcesCreatedByEmployee ()

Get all opt in list sources

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
    public class FetchOptInListSourcesCreatedByEmployeeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Get all opt in list sources
                List<OptInListSource> result = apiInstance.FetchOptInListSourcesCreatedByEmployee();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchOptInListSourcesCreatedByEmployee: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchOptInListSourcesCreatedByEmployeeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all opt in list sources
    ApiResponse<List<OptInListSource>> response = apiInstance.FetchOptInListSourcesCreatedByEmployeeWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchOptInListSourcesCreatedByEmployeeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;OptInListSource&gt;**](OptInListSource.md)

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

<a id="fetchpeeractivity"></a>
# **FetchPeerActivity**
> List&lt;EmployeeActivityLog&gt; FetchPeerActivity (string employeeID)

Get peer activity

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
    public class FetchPeerActivityExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var employeeID = "employeeID_example";  // string | 

            try
            {
                // Get peer activity
                List<EmployeeActivityLog> result = apiInstance.FetchPeerActivity(employeeID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchPeerActivity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchPeerActivityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get peer activity
    ApiResponse<List<EmployeeActivityLog>> response = apiInstance.FetchPeerActivityWithHttpInfo(employeeID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchPeerActivityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **employeeID** | **string** |  |  |

### Return type

[**List&lt;EmployeeActivityLog&gt;**](EmployeeActivityLog.md)

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

<a id="fetchpeerspermissions"></a>
# **FetchPeersPermissions**
> List&lt;Object&gt; FetchPeersPermissions (string userID)

Get peer permissions

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
    public class FetchPeersPermissionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var userID = "userID_example";  // string | 

            try
            {
                // Get peer permissions
                List<Object> result = apiInstance.FetchPeersPermissions(userID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchPeersPermissions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchPeersPermissionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get peer permissions
    ApiResponse<List<Object>> response = apiInstance.FetchPeersPermissionsWithHttpInfo(userID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchPeersPermissionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userID** | **string** |  |  |

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

<a id="fetchprofileinfo"></a>
# **FetchProfileInfo**
> Employee FetchProfileInfo ()

Get employee info

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
    public class FetchProfileInfoExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Get employee info
                Employee result = apiInstance.FetchProfileInfo();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.FetchProfileInfo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FetchProfileInfoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get employee info
    ApiResponse<Employee> response = apiInstance.FetchProfileInfoWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.FetchProfileInfoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**Employee**](Employee.md)

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

<a id="importclubmembers"></a>
# **ImportClubMembers**
> string ImportClubMembers (WTEmployeeImportRecords wTEmployeeImportRecords)

Import club members

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
    public class ImportClubMembersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeImportRecords = new WTEmployeeImportRecords(); // WTEmployeeImportRecords | 

            try
            {
                // Import club members
                string result = apiInstance.ImportClubMembers(wTEmployeeImportRecords);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ImportClubMembers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImportClubMembersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Import club members
    ApiResponse<string> response = apiInstance.ImportClubMembersWithHttpInfo(wTEmployeeImportRecords);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ImportClubMembersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
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

<a id="importmerchantcredits"></a>
# **ImportMerchantCredits**
> string ImportMerchantCredits (WTEmployeeImportRecords wTEmployeeImportRecords)

Import merchant credits

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
    public class ImportMerchantCreditsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeImportRecords = new WTEmployeeImportRecords(); // WTEmployeeImportRecords | 

            try
            {
                // Import merchant credits
                string result = apiInstance.ImportMerchantCredits(wTEmployeeImportRecords);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ImportMerchantCredits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImportMerchantCreditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Import merchant credits
    ApiResponse<string> response = apiInstance.ImportMerchantCreditsWithHttpInfo(wTEmployeeImportRecords);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ImportMerchantCreditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
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

<a id="loadwebpagesofemployee"></a>
# **LoadWebpagesOfEmployee**
> List&lt;Webpage&gt; LoadWebpagesOfEmployee ()

Get employee's permissions

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
    public class LoadWebpagesOfEmployeeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Get employee's permissions
                List<Webpage> result = apiInstance.LoadWebpagesOfEmployee();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.LoadWebpagesOfEmployee: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoadWebpagesOfEmployeeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get employee's permissions
    ApiResponse<List<Webpage>> response = apiInstance.LoadWebpagesOfEmployeeWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.LoadWebpagesOfEmployeeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;Webpage&gt;**](Webpage.md)

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

<a id="modifypeersroles"></a>
# **ModifyPeersRoles**
> List&lt;Object&gt; ModifyPeersRoles (string userID, WTEmployeePeerRoles wTEmployeePeerRoles)

Modify peer's roles

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
    public class ModifyPeersRolesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var userID = "userID_example";  // string | 
            var wTEmployeePeerRoles = new WTEmployeePeerRoles(); // WTEmployeePeerRoles | 

            try
            {
                // Modify peer's roles
                List<Object> result = apiInstance.ModifyPeersRoles(userID, wTEmployeePeerRoles);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ModifyPeersRoles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ModifyPeersRolesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Modify peer's roles
    ApiResponse<List<Object>> response = apiInstance.ModifyPeersRolesWithHttpInfo(userID, wTEmployeePeerRoles);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ModifyPeersRolesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userID** | **string** |  |  |
| **wTEmployeePeerRoles** | [**WTEmployeePeerRoles**](WTEmployeePeerRoles.md) |  |  |

### Return type

**List<Object>**

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

<a id="presignfile"></a>
# **PresignFile**
> PresignedPost PresignFile (WTEmployeeS3FilePresign wTEmployeeS3FilePresign)

Presign file for upload

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
    public class PresignFileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeS3FilePresign = new WTEmployeeS3FilePresign(); // WTEmployeeS3FilePresign | 

            try
            {
                // Presign file for upload
                PresignedPost result = apiInstance.PresignFile(wTEmployeeS3FilePresign);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.PresignFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PresignFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Presign file for upload
    ApiResponse<PresignedPost> response = apiInstance.PresignFileWithHttpInfo(wTEmployeeS3FilePresign);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.PresignFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeS3FilePresign** | [**WTEmployeeS3FilePresign**](WTEmployeeS3FilePresign.md) |  |  |

### Return type

[**PresignedPost**](PresignedPost.md)

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

<a id="removepeerfromallroles"></a>
# **RemovePeerFromAllRoles**
> bool RemovePeerFromAllRoles (string userID)

Remove peer from all roles

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
    public class RemovePeerFromAllRolesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var userID = "userID_example";  // string | 

            try
            {
                // Remove peer from all roles
                bool result = apiInstance.RemovePeerFromAllRoles(userID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.RemovePeerFromAllRoles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemovePeerFromAllRolesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove peer from all roles
    ApiResponse<bool> response = apiInstance.RemovePeerFromAllRolesWithHttpInfo(userID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.RemovePeerFromAllRolesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userID** | **string** |  |  |

### Return type

**bool**

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

<a id="scheduleadvertisementcredit"></a>
# **ScheduleAdvertisementCredit**
> AdvertisementCreditBroadcast ScheduleAdvertisementCredit (string advertisementCreditID, WTEmployeeScheduleSimpleSMS wTEmployeeScheduleSimpleSMS)

Schedule Ad Credit

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
    public class ScheduleAdvertisementCreditExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var advertisementCreditID = "advertisementCreditID_example";  // string | 
            var wTEmployeeScheduleSimpleSMS = new WTEmployeeScheduleSimpleSMS(); // WTEmployeeScheduleSimpleSMS | 

            try
            {
                // Schedule Ad Credit
                AdvertisementCreditBroadcast result = apiInstance.ScheduleAdvertisementCredit(advertisementCreditID, wTEmployeeScheduleSimpleSMS);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ScheduleAdvertisementCredit: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleAdvertisementCreditWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Ad Credit
    ApiResponse<AdvertisementCreditBroadcast> response = apiInstance.ScheduleAdvertisementCreditWithHttpInfo(advertisementCreditID, wTEmployeeScheduleSimpleSMS);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ScheduleAdvertisementCreditWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **advertisementCreditID** | **string** |  |  |
| **wTEmployeeScheduleSimpleSMS** | [**WTEmployeeScheduleSimpleSMS**](WTEmployeeScheduleSimpleSMS.md) |  |  |

### Return type

[**AdvertisementCreditBroadcast**](AdvertisementCreditBroadcast.md)

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
| **413** | Entity Too Large |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="scheduledynamicvoucher"></a>
# **ScheduleDynamicVoucher**
> DynamicVoucherBroadcast ScheduleDynamicVoucher (string dynamicVoucherID, WTEmployeeScheduleSimpleSMS wTEmployeeScheduleSimpleSMS)

Schedule Dynamic Voucher to list

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
    public class ScheduleDynamicVoucherExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var dynamicVoucherID = "dynamicVoucherID_example";  // string | 
            var wTEmployeeScheduleSimpleSMS = new WTEmployeeScheduleSimpleSMS(); // WTEmployeeScheduleSimpleSMS | 

            try
            {
                // Schedule Dynamic Voucher to list
                DynamicVoucherBroadcast result = apiInstance.ScheduleDynamicVoucher(dynamicVoucherID, wTEmployeeScheduleSimpleSMS);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ScheduleDynamicVoucher: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleDynamicVoucherWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Dynamic Voucher to list
    ApiResponse<DynamicVoucherBroadcast> response = apiInstance.ScheduleDynamicVoucherWithHttpInfo(dynamicVoucherID, wTEmployeeScheduleSimpleSMS);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ScheduleDynamicVoucherWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dynamicVoucherID** | **string** |  |  |
| **wTEmployeeScheduleSimpleSMS** | [**WTEmployeeScheduleSimpleSMS**](WTEmployeeScheduleSimpleSMS.md) |  |  |

### Return type

[**DynamicVoucherBroadcast**](DynamicVoucherBroadcast.md)

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
| **413** | Entity Too Large |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="scheduledynamicvouchertorecipient"></a>
# **ScheduleDynamicVoucherToRecipient**
> DynamicVoucherBroadcast ScheduleDynamicVoucherToRecipient (string dynamicVoucherID, WTEmployeeScheduleSimpleSMSToRecipient wTEmployeeScheduleSimpleSMSToRecipient)

Schedule Dyanamic Voucher to recipient

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
    public class ScheduleDynamicVoucherToRecipientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var dynamicVoucherID = "dynamicVoucherID_example";  // string | 
            var wTEmployeeScheduleSimpleSMSToRecipient = new WTEmployeeScheduleSimpleSMSToRecipient(); // WTEmployeeScheduleSimpleSMSToRecipient | 

            try
            {
                // Schedule Dyanamic Voucher to recipient
                DynamicVoucherBroadcast result = apiInstance.ScheduleDynamicVoucherToRecipient(dynamicVoucherID, wTEmployeeScheduleSimpleSMSToRecipient);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ScheduleDynamicVoucherToRecipient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleDynamicVoucherToRecipientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Dyanamic Voucher to recipient
    ApiResponse<DynamicVoucherBroadcast> response = apiInstance.ScheduleDynamicVoucherToRecipientWithHttpInfo(dynamicVoucherID, wTEmployeeScheduleSimpleSMSToRecipient);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ScheduleDynamicVoucherToRecipientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dynamicVoucherID** | **string** |  |  |
| **wTEmployeeScheduleSimpleSMSToRecipient** | [**WTEmployeeScheduleSimpleSMSToRecipient**](WTEmployeeScheduleSimpleSMSToRecipient.md) |  |  |

### Return type

[**DynamicVoucherBroadcast**](DynamicVoucherBroadcast.md)

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
| **413** | Entity Too Large |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="schedulesimplesms"></a>
# **ScheduleSimpleSMS**
> bool ScheduleSimpleSMS (WTEmployeeScheduleSimpleSMS wTEmployeeScheduleSimpleSMS)

Schedule Simple SMS broadcast to list

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
    public class ScheduleSimpleSMSExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeScheduleSimpleSMS = new WTEmployeeScheduleSimpleSMS(); // WTEmployeeScheduleSimpleSMS | 

            try
            {
                // Schedule Simple SMS broadcast to list
                bool result = apiInstance.ScheduleSimpleSMS(wTEmployeeScheduleSimpleSMS);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ScheduleSimpleSMS: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleSimpleSMSWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Simple SMS broadcast to list
    ApiResponse<bool> response = apiInstance.ScheduleSimpleSMSWithHttpInfo(wTEmployeeScheduleSimpleSMS);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ScheduleSimpleSMSWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeScheduleSimpleSMS** | [**WTEmployeeScheduleSimpleSMS**](WTEmployeeScheduleSimpleSMS.md) |  |  |

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
| **413** | Entity Too Large |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="schedulesimplesmstorecipient"></a>
# **ScheduleSimpleSMSToRecipient**
> bool ScheduleSimpleSMSToRecipient (WTEmployeeScheduleSimpleSMSToRecipient wTEmployeeScheduleSimpleSMSToRecipient)

Schedule Simple SMS broadcast to recipient

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
    public class ScheduleSimpleSMSToRecipientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeScheduleSimpleSMSToRecipient = new WTEmployeeScheduleSimpleSMSToRecipient(); // WTEmployeeScheduleSimpleSMSToRecipient | 

            try
            {
                // Schedule Simple SMS broadcast to recipient
                bool result = apiInstance.ScheduleSimpleSMSToRecipient(wTEmployeeScheduleSimpleSMSToRecipient);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.ScheduleSimpleSMSToRecipient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ScheduleSimpleSMSToRecipientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule Simple SMS broadcast to recipient
    ApiResponse<bool> response = apiInstance.ScheduleSimpleSMSToRecipientWithHttpInfo(wTEmployeeScheduleSimpleSMSToRecipient);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.ScheduleSimpleSMSToRecipientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeScheduleSimpleSMSToRecipient** | [**WTEmployeeScheduleSimpleSMSToRecipient**](WTEmployeeScheduleSimpleSMSToRecipient.md) |  |  |

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
| **413** | Entity Too Large |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sendhelpdeskresponse"></a>
# **SendHelpDeskResponse**
> OutboundSMS SendHelpDeskResponse (WTEmployeeSendHelpDeskResponse wTEmployeeSendHelpDeskResponse)

Send help desk response

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
    public class SendHelpDeskResponseExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeSendHelpDeskResponse = new WTEmployeeSendHelpDeskResponse(); // WTEmployeeSendHelpDeskResponse | 

            try
            {
                // Send help desk response
                OutboundSMS result = apiInstance.SendHelpDeskResponse(wTEmployeeSendHelpDeskResponse);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.SendHelpDeskResponse: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendHelpDeskResponseWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send help desk response
    ApiResponse<OutboundSMS> response = apiInstance.SendHelpDeskResponseWithHttpInfo(wTEmployeeSendHelpDeskResponse);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.SendHelpDeskResponseWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeSendHelpDeskResponse** | [**WTEmployeeSendHelpDeskResponse**](WTEmployeeSendHelpDeskResponse.md) |  |  |

### Return type

[**OutboundSMS**](OutboundSMS.md)

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

<a id="sendsmscampaignbroadcast"></a>
# **SendSmsCampaignBroadcast**
> StaticVoucherCampaignBroadcast SendSmsCampaignBroadcast (string staticVoucherCampaignID, WTEmployeeScheduleSMSCampaignBroadcast wTEmployeeScheduleSMSCampaignBroadcast)

Schedule SMS Campaign Broadcast

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
    public class SendSmsCampaignBroadcastExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var staticVoucherCampaignID = "staticVoucherCampaignID_example";  // string | 
            var wTEmployeeScheduleSMSCampaignBroadcast = new WTEmployeeScheduleSMSCampaignBroadcast(); // WTEmployeeScheduleSMSCampaignBroadcast | 

            try
            {
                // Schedule SMS Campaign Broadcast
                StaticVoucherCampaignBroadcast result = apiInstance.SendSmsCampaignBroadcast(staticVoucherCampaignID, wTEmployeeScheduleSMSCampaignBroadcast);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.SendSmsCampaignBroadcast: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendSmsCampaignBroadcastWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Schedule SMS Campaign Broadcast
    ApiResponse<StaticVoucherCampaignBroadcast> response = apiInstance.SendSmsCampaignBroadcastWithHttpInfo(staticVoucherCampaignID, wTEmployeeScheduleSMSCampaignBroadcast);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.SendSmsCampaignBroadcastWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **staticVoucherCampaignID** | **string** |  |  |
| **wTEmployeeScheduleSMSCampaignBroadcast** | [**WTEmployeeScheduleSMSCampaignBroadcast**](WTEmployeeScheduleSMSCampaignBroadcast.md) |  |  |

### Return type

[**StaticVoucherCampaignBroadcast**](StaticVoucherCampaignBroadcast.md)

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
| **413** | Entity Too Large |  -  |
| **422** | Validation Failed |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setalertsread"></a>
# **SetAlertsRead**
> bool SetAlertsRead ()

Mark alerts as read

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
    public class SetAlertsReadExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Mark alerts as read
                bool result = apiInstance.SetAlertsRead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.SetAlertsRead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetAlertsReadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark alerts as read
    ApiResponse<bool> response = apiInstance.SetAlertsReadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.SetAlertsReadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**bool**

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

<a id="setexportdatafilesread"></a>
# **SetExportDataFilesRead**
> bool SetExportDataFilesRead ()

Mark export data files as read

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
    public class SetExportDataFilesReadExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Mark export data files as read
                bool result = apiInstance.SetExportDataFilesRead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.SetExportDataFilesRead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetExportDataFilesReadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark export data files as read
    ApiResponse<bool> response = apiInstance.SetExportDataFilesReadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.SetExportDataFilesReadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**bool**

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

<a id="sethelpdeskrequestresolved"></a>
# **SetHelpDeskRequestResolved**
> HelpDeskRequest SetHelpDeskRequestResolved (string helpDeskRequestID)

Resolve help desk request

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
    public class SetHelpDeskRequestResolvedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var helpDeskRequestID = "helpDeskRequestID_example";  // string | 

            try
            {
                // Resolve help desk request
                HelpDeskRequest result = apiInstance.SetHelpDeskRequestResolved(helpDeskRequestID);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.SetHelpDeskRequestResolved: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetHelpDeskRequestResolvedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resolve help desk request
    ApiResponse<HelpDeskRequest> response = apiInstance.SetHelpDeskRequestResolvedWithHttpInfo(helpDeskRequestID);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.SetHelpDeskRequestResolvedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **helpDeskRequestID** | **string** |  |  |

### Return type

[**HelpDeskRequest**](HelpDeskRequest.md)

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

<a id="setmessagesread"></a>
# **SetMessagesRead**
> bool SetMessagesRead ()

Mark messages as read

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
    public class SetMessagesReadExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);

            try
            {
                // Mark messages as read
                bool result = apiInstance.SetMessagesRead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.SetMessagesRead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetMessagesReadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark messages as read
    ApiResponse<bool> response = apiInstance.SetMessagesReadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.SetMessagesReadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**bool**

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

<a id="setprofilepicture"></a>
# **SetProfilePicture**
> string SetProfilePicture (WTEmployeeCreateMediaFile wTEmployeeCreateMediaFile)

Set profile picture

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
    public class SetProfilePictureExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeCreateMediaFile = new WTEmployeeCreateMediaFile(); // WTEmployeeCreateMediaFile | 

            try
            {
                // Set profile picture
                string result = apiInstance.SetProfilePicture(wTEmployeeCreateMediaFile);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.SetProfilePicture: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetProfilePictureWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set profile picture
    ApiResponse<string> response = apiInstance.SetProfilePictureWithHttpInfo(wTEmployeeCreateMediaFile);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.SetProfilePictureWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeCreateMediaFile** | [**WTEmployeeCreateMediaFile**](WTEmployeeCreateMediaFile.md) |  |  |

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

<a id="updateclubmembers"></a>
# **UpdateClubMembers**
> string UpdateClubMembers (WTEmployeeUpdateRecords wTEmployeeUpdateRecords)

Update club members

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
    public class UpdateClubMembersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var wTEmployeeUpdateRecords = new WTEmployeeUpdateRecords(); // WTEmployeeUpdateRecords | 

            try
            {
                // Update club members
                string result = apiInstance.UpdateClubMembers(wTEmployeeUpdateRecords);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.UpdateClubMembers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateClubMembersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update club members
    ApiResponse<string> response = apiInstance.UpdateClubMembersWithHttpInfo(wTEmployeeUpdateRecords);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.UpdateClubMembersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTEmployeeUpdateRecords** | [**WTEmployeeUpdateRecords**](WTEmployeeUpdateRecords.md) |  |  |

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

<a id="updateemailnotificationpreference"></a>
# **UpdateEmailNotificationPreference**
> Employee UpdateEmailNotificationPreference (UpdateEmailNotificationPreferenceRequest updateEmailNotificationPreferenceRequest)

Changes the employee's email notification preference to enabled or disabled

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
    public class UpdateEmailNotificationPreferenceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var updateEmailNotificationPreferenceRequest = new UpdateEmailNotificationPreferenceRequest(); // UpdateEmailNotificationPreferenceRequest | 

            try
            {
                // Changes the employee's email notification preference to enabled or disabled
                Employee result = apiInstance.UpdateEmailNotificationPreference(updateEmailNotificationPreferenceRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.UpdateEmailNotificationPreference: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEmailNotificationPreferenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Changes the employee's email notification preference to enabled or disabled
    ApiResponse<Employee> response = apiInstance.UpdateEmailNotificationPreferenceWithHttpInfo(updateEmailNotificationPreferenceRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.UpdateEmailNotificationPreferenceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateEmailNotificationPreferenceRequest** | [**UpdateEmailNotificationPreferenceRequest**](UpdateEmailNotificationPreferenceRequest.md) |  |  |

### Return type

[**Employee**](Employee.md)

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

<a id="updateemployeepeer"></a>
# **UpdateEmployeePeer**
> Employee UpdateEmployeePeer (string userID, WTEmployeeUpdate wTEmployeeUpdate)

Update peer

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
    public class UpdateEmployeePeerExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new EmployeesApi(httpClient, config, httpClientHandler);
            var userID = "userID_example";  // string | 
            var wTEmployeeUpdate = new WTEmployeeUpdate(); // WTEmployeeUpdate | 

            try
            {
                // Update peer
                Employee result = apiInstance.UpdateEmployeePeer(userID, wTEmployeeUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EmployeesApi.UpdateEmployeePeer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEmployeePeerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update peer
    ApiResponse<Employee> response = apiInstance.UpdateEmployeePeerWithHttpInfo(userID, wTEmployeeUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EmployeesApi.UpdateEmployeePeerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userID** | **string** |  |  |
| **wTEmployeeUpdate** | [**WTEmployeeUpdate**](WTEmployeeUpdate.md) |  |  |

### Return type

[**Employee**](Employee.md)

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

