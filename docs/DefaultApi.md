# WalletInc.Api.DefaultApi

All URIs are relative to *https://api.wall.et*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CustomersDynamicVoucherRedeemed**](DefaultApi.md#customersdynamicvoucherredeemed) | **POST** /Customers.DynamicVoucher.redeemed |  |
| [**CustomersDynamicVoucherRefunded**](DefaultApi.md#customersdynamicvoucherrefunded) | **POST** /Customers.DynamicVoucher.refunded |  |
| [**CustomersMerchantCreditRedeemed**](DefaultApi.md#customersmerchantcreditredeemed) | **POST** /Customers.MerchantCredit.redeemed |  |
| [**CustomersMerchantCreditRefunded**](DefaultApi.md#customersmerchantcreditrefunded) | **POST** /Customers.MerchantCredit.refunded |  |
| [**CustomersPrizeRedeemed**](DefaultApi.md#customersprizeredeemed) | **POST** /Customers.Prize.redeemed |  |
| [**CustomersPrizeRefunded**](DefaultApi.md#customersprizerefunded) | **POST** /Customers.Prize.refunded |  |
| [**CustomersStaticVoucherRedeemed**](DefaultApi.md#customersstaticvoucherredeemed) | **POST** /Customers.StaticVoucher.redeemed |  |
| [**CustomersStaticVoucherRefunded**](DefaultApi.md#customersstaticvoucherrefunded) | **POST** /Customers.StaticVoucher.refunded |  |
| [**CustomersTicketClaimed**](DefaultApi.md#customersticketclaimed) | **POST** /Customers.Ticket.claimed |  |
| [**CustomersTicketRedeemed**](DefaultApi.md#customersticketredeemed) | **POST** /Customers.Ticket.redeemed |  |
| [**CustomersTicketUnclaimed**](DefaultApi.md#customersticketunclaimed) | **POST** /Customers.Ticket.unclaimed |  |
| [**MembersPointsRedeemed**](DefaultApi.md#memberspointsredeemed) | **POST** /Members.Points.redeemed |  |
| [**MembersPointsRefunded**](DefaultApi.md#memberspointsrefunded) | **POST** /Members.Points.refunded |  |
| [**MembersTierRedeemed**](DefaultApi.md#memberstierredeemed) | **POST** /Members.Tier.redeemed |  |
| [**MembersTierRefunded**](DefaultApi.md#memberstierrefunded) | **POST** /Members.Tier.refunded |  |
| [**SubscribersEmailOptIn**](DefaultApi.md#subscribersemailoptin) | **POST** /Subscribers.Email.opt_in |  |
| [**SubscribersSMSDefaultOptIn**](DefaultApi.md#subscriberssmsdefaultoptin) | **POST** /Subscribers.SMS.default_opt_in |  |
| [**SubscribersSMSKeywordOptIn**](DefaultApi.md#subscriberssmskeywordoptin) | **POST** /Subscribers.SMS.keyword_opt_in |  |
| [**VisitorsAuthentiationSuccess**](DefaultApi.md#visitorsauthentiationsuccess) | **POST** /Visitors.Authentiation.success |  |
| [**VisitorsBusinessCardDownloaded**](DefaultApi.md#visitorsbusinesscarddownloaded) | **POST** /Visitors.BusinessCard.downloaded |  |
| [**VisitorsCalendarEventDownloaded**](DefaultApi.md#visitorscalendareventdownloaded) | **POST** /Visitors.CalendarEvent.downloaded |  |
| [**WalletPlatformAddOnPurchased**](DefaultApi.md#walletplatformaddonpurchased) | **POST** /WalletPlatform.AddOn.purchased |  |
| [**WalletPlatformInvoiceCreated**](DefaultApi.md#walletplatforminvoicecreated) | **POST** /WalletPlatform.Invoice.created |  |
| [**WalletPlatformInvoicePaid**](DefaultApi.md#walletplatforminvoicepaid) | **POST** /WalletPlatform.Invoice.paid |  |
| [**WalletPlatformLedgerEntryCreated**](DefaultApi.md#walletplatformledgerentrycreated) | **POST** /WalletPlatform.LedgerEntry.created |  |
| [**WalletPlatformPaymentMethodAdded**](DefaultApi.md#walletplatformpaymentmethodadded) | **POST** /WalletPlatform.PaymentMethod.added |  |
| [**WalletPlatformSubscriptionChanged**](DefaultApi.md#walletplatformsubscriptionchanged) | **POST** /WalletPlatform.Subscription.changed |  |

<a id="customersdynamicvoucherredeemed"></a>
# **CustomersDynamicVoucherRedeemed**
> void CustomersDynamicVoucherRedeemed (DynamicVoucher? dynamicVoucher = null)



A customer just redeemed a Dynamic Voucher.

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
    public class CustomersDynamicVoucherRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var dynamicVoucher = new DynamicVoucher?(); // DynamicVoucher? |  (optional) 

            try
            {
                apiInstance.CustomersDynamicVoucherRedeemed(dynamicVoucher);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersDynamicVoucherRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersDynamicVoucherRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersDynamicVoucherRedeemedWithHttpInfo(dynamicVoucher);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersDynamicVoucherRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dynamicVoucher** | [**DynamicVoucher?**](DynamicVoucher?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersdynamicvoucherrefunded"></a>
# **CustomersDynamicVoucherRefunded**
> void CustomersDynamicVoucherRefunded (DynamicVoucher? dynamicVoucher = null)



A Dynamic Voucher was just refunded to the customer.

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
    public class CustomersDynamicVoucherRefundedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var dynamicVoucher = new DynamicVoucher?(); // DynamicVoucher? |  (optional) 

            try
            {
                apiInstance.CustomersDynamicVoucherRefunded(dynamicVoucher);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersDynamicVoucherRefunded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersDynamicVoucherRefundedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersDynamicVoucherRefundedWithHttpInfo(dynamicVoucher);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersDynamicVoucherRefundedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dynamicVoucher** | [**DynamicVoucher?**](DynamicVoucher?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersmerchantcreditredeemed"></a>
# **CustomersMerchantCreditRedeemed**
> void CustomersMerchantCreditRedeemed (WTMerchantCredit? wTMerchantCredit = null)



A customer just redeemed some Merchant Credit.

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
    public class CustomersMerchantCreditRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var wTMerchantCredit = new WTMerchantCredit?(); // WTMerchantCredit? |  (optional) 

            try
            {
                apiInstance.CustomersMerchantCreditRedeemed(wTMerchantCredit);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersMerchantCreditRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersMerchantCreditRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersMerchantCreditRedeemedWithHttpInfo(wTMerchantCredit);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersMerchantCreditRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMerchantCredit** | [**WTMerchantCredit?**](WTMerchantCredit?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersmerchantcreditrefunded"></a>
# **CustomersMerchantCreditRefunded**
> void CustomersMerchantCreditRefunded (WTMerchantCredit? wTMerchantCredit = null)



Merchant Credit was just refunded to a customer.

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
    public class CustomersMerchantCreditRefundedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var wTMerchantCredit = new WTMerchantCredit?(); // WTMerchantCredit? |  (optional) 

            try
            {
                apiInstance.CustomersMerchantCreditRefunded(wTMerchantCredit);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersMerchantCreditRefunded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersMerchantCreditRefundedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersMerchantCreditRefundedWithHttpInfo(wTMerchantCredit);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersMerchantCreditRefundedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMerchantCredit** | [**WTMerchantCredit?**](WTMerchantCredit?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersprizeredeemed"></a>
# **CustomersPrizeRedeemed**
> void CustomersPrizeRedeemed (AdvertisementCreditScan? advertisementCreditScan = null)



A customer just redeemed a Prize.

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
    public class CustomersPrizeRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var advertisementCreditScan = new AdvertisementCreditScan?(); // AdvertisementCreditScan? |  (optional) 

            try
            {
                apiInstance.CustomersPrizeRedeemed(advertisementCreditScan);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersPrizeRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersPrizeRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersPrizeRedeemedWithHttpInfo(advertisementCreditScan);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersPrizeRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **advertisementCreditScan** | [**AdvertisementCreditScan?**](AdvertisementCreditScan?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersprizerefunded"></a>
# **CustomersPrizeRefunded**
> void CustomersPrizeRefunded (AdvertisementCreditScan? advertisementCreditScan = null)



A Prize was just refunded to the customer.

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
    public class CustomersPrizeRefundedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var advertisementCreditScan = new AdvertisementCreditScan?(); // AdvertisementCreditScan? |  (optional) 

            try
            {
                apiInstance.CustomersPrizeRefunded(advertisementCreditScan);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersPrizeRefunded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersPrizeRefundedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersPrizeRefundedWithHttpInfo(advertisementCreditScan);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersPrizeRefundedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **advertisementCreditScan** | [**AdvertisementCreditScan?**](AdvertisementCreditScan?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersstaticvoucherredeemed"></a>
# **CustomersStaticVoucherRedeemed**
> void CustomersStaticVoucherRedeemed (StaticVoucher? staticVoucher = null)



A customer just redeemed a Static Voucher.

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
    public class CustomersStaticVoucherRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var staticVoucher = new StaticVoucher?(); // StaticVoucher? |  (optional) 

            try
            {
                apiInstance.CustomersStaticVoucherRedeemed(staticVoucher);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersStaticVoucherRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersStaticVoucherRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersStaticVoucherRedeemedWithHttpInfo(staticVoucher);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersStaticVoucherRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **staticVoucher** | [**StaticVoucher?**](StaticVoucher?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersstaticvoucherrefunded"></a>
# **CustomersStaticVoucherRefunded**
> void CustomersStaticVoucherRefunded (StaticVoucher? staticVoucher = null)



A Static Voucher was just refunded to the customer.

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
    public class CustomersStaticVoucherRefundedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var staticVoucher = new StaticVoucher?(); // StaticVoucher? |  (optional) 

            try
            {
                apiInstance.CustomersStaticVoucherRefunded(staticVoucher);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersStaticVoucherRefunded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersStaticVoucherRefundedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersStaticVoucherRefundedWithHttpInfo(staticVoucher);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersStaticVoucherRefundedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **staticVoucher** | [**StaticVoucher?**](StaticVoucher?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersticketclaimed"></a>
# **CustomersTicketClaimed**
> void CustomersTicketClaimed (Ticket? ticket = null)



A customer just claimed a Ticket.

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
    public class CustomersTicketClaimedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var ticket = new Ticket?(); // Ticket? |  (optional) 

            try
            {
                apiInstance.CustomersTicketClaimed(ticket);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersTicketClaimed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersTicketClaimedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersTicketClaimedWithHttpInfo(ticket);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersTicketClaimedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ticket** | [**Ticket?**](Ticket?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersticketredeemed"></a>
# **CustomersTicketRedeemed**
> void CustomersTicketRedeemed (Ticket? ticket = null)



A customer just redeemed a Ticket.

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
    public class CustomersTicketRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var ticket = new Ticket?(); // Ticket? |  (optional) 

            try
            {
                apiInstance.CustomersTicketRedeemed(ticket);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersTicketRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersTicketRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersTicketRedeemedWithHttpInfo(ticket);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersTicketRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ticket** | [**Ticket?**](Ticket?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersticketunclaimed"></a>
# **CustomersTicketUnclaimed**
> void CustomersTicketUnclaimed (Ticket? ticket = null)



A customer just unclaimed a Ticket.

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
    public class CustomersTicketUnclaimedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var ticket = new Ticket?(); // Ticket? |  (optional) 

            try
            {
                apiInstance.CustomersTicketUnclaimed(ticket);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.CustomersTicketUnclaimed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersTicketUnclaimedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.CustomersTicketUnclaimedWithHttpInfo(ticket);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.CustomersTicketUnclaimedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ticket** | [**Ticket?**](Ticket?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="memberspointsredeemed"></a>
# **MembersPointsRedeemed**
> void MembersPointsRedeemed (Member? member = null)



A member just redeemed some Membership Points.

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
    public class MembersPointsRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var member = new Member?(); // Member? |  (optional) 

            try
            {
                apiInstance.MembersPointsRedeemed(member);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.MembersPointsRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MembersPointsRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.MembersPointsRedeemedWithHttpInfo(member);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.MembersPointsRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **member** | [**Member?**](Member?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="memberspointsrefunded"></a>
# **MembersPointsRefunded**
> void MembersPointsRefunded (Member? member = null)



Membership Points were just refunded to a member.

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
    public class MembersPointsRefundedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var member = new Member?(); // Member? |  (optional) 

            try
            {
                apiInstance.MembersPointsRefunded(member);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.MembersPointsRefunded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MembersPointsRefundedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.MembersPointsRefundedWithHttpInfo(member);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.MembersPointsRefundedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **member** | [**Member?**](Member?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="memberstierredeemed"></a>
# **MembersTierRedeemed**
> void MembersTierRedeemed (WTMembershipTier? wTMembershipTier = null)



A member just redeemed a Membership Tier discount.

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
    public class MembersTierRedeemedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var wTMembershipTier = new WTMembershipTier?(); // WTMembershipTier? |  (optional) 

            try
            {
                apiInstance.MembersTierRedeemed(wTMembershipTier);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.MembersTierRedeemed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MembersTierRedeemedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.MembersTierRedeemedWithHttpInfo(wTMembershipTier);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.MembersTierRedeemedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMembershipTier** | [**WTMembershipTier?**](WTMembershipTier?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="memberstierrefunded"></a>
# **MembersTierRefunded**
> void MembersTierRefunded (WTMembershipTier? wTMembershipTier = null)



A Membership Tier discount was just refunded to a member.

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
    public class MembersTierRefundedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var wTMembershipTier = new WTMembershipTier?(); // WTMembershipTier? |  (optional) 

            try
            {
                apiInstance.MembersTierRefunded(wTMembershipTier);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.MembersTierRefunded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MembersTierRefundedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.MembersTierRefundedWithHttpInfo(wTMembershipTier);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.MembersTierRefundedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **wTMembershipTier** | [**WTMembershipTier?**](WTMembershipTier?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscribersemailoptin"></a>
# **SubscribersEmailOptIn**
> void SubscribersEmailOptIn (EmailSubscriber? emailSubscriber = null)



A new subscriber has opted-in to receive your email communications.

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
    public class SubscribersEmailOptInExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var emailSubscriber = new EmailSubscriber?(); // EmailSubscriber? |  (optional) 

            try
            {
                apiInstance.SubscribersEmailOptIn(emailSubscriber);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.SubscribersEmailOptIn: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscribersEmailOptInWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.SubscribersEmailOptInWithHttpInfo(emailSubscriber);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.SubscribersEmailOptInWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **emailSubscriber** | [**EmailSubscriber?**](EmailSubscriber?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscriberssmsdefaultoptin"></a>
# **SubscribersSMSDefaultOptIn**
> void SubscribersSMSDefaultOptIn (SmsSubscriber? smsSubscriber = null)



A new subscriber has opted-in to your default SMS/MMS subscriber list.

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
    public class SubscribersSMSDefaultOptInExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var smsSubscriber = new SmsSubscriber?(); // SmsSubscriber? |  (optional) 

            try
            {
                apiInstance.SubscribersSMSDefaultOptIn(smsSubscriber);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.SubscribersSMSDefaultOptIn: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscribersSMSDefaultOptInWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.SubscribersSMSDefaultOptInWithHttpInfo(smsSubscriber);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.SubscribersSMSDefaultOptInWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **smsSubscriber** | [**SmsSubscriber?**](SmsSubscriber?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscriberssmskeywordoptin"></a>
# **SubscribersSMSKeywordOptIn**
> void SubscribersSMSKeywordOptIn (OptInListSubscriber? optInListSubscriber = null)



A new subscriber has opted-in to a specific list / keyword for specialised SMS/MMS communications.

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
    public class SubscribersSMSKeywordOptInExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var optInListSubscriber = new OptInListSubscriber?(); // OptInListSubscriber? |  (optional) 

            try
            {
                apiInstance.SubscribersSMSKeywordOptIn(optInListSubscriber);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.SubscribersSMSKeywordOptIn: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscribersSMSKeywordOptInWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.SubscribersSMSKeywordOptInWithHttpInfo(optInListSubscriber);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.SubscribersSMSKeywordOptInWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **optInListSubscriber** | [**OptInListSubscriber?**](OptInListSubscriber?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="visitorsauthentiationsuccess"></a>
# **VisitorsAuthentiationSuccess**
> void VisitorsAuthentiationSuccess ()



A visitor successfully authenticated with their mobile phone number and is now a recognized customer.

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
    public class VisitorsAuthentiationSuccessExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.VisitorsAuthentiationSuccess();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.VisitorsAuthentiationSuccess: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VisitorsAuthentiationSuccessWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.VisitorsAuthentiationSuccessWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.VisitorsAuthentiationSuccessWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="visitorsbusinesscarddownloaded"></a>
# **VisitorsBusinessCardDownloaded**
> void VisitorsBusinessCardDownloaded ()



A visitor downloaded a Virtual Business Card.

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
    public class VisitorsBusinessCardDownloadedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.VisitorsBusinessCardDownloaded();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.VisitorsBusinessCardDownloaded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VisitorsBusinessCardDownloadedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.VisitorsBusinessCardDownloadedWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.VisitorsBusinessCardDownloadedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="visitorscalendareventdownloaded"></a>
# **VisitorsCalendarEventDownloaded**
> void VisitorsCalendarEventDownloaded ()



A visitor downloaded a calendar reminder for one of your upcoming events.

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
    public class VisitorsCalendarEventDownloadedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.VisitorsCalendarEventDownloaded();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.VisitorsCalendarEventDownloaded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VisitorsCalendarEventDownloadedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.VisitorsCalendarEventDownloadedWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.VisitorsCalendarEventDownloadedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="walletplatformaddonpurchased"></a>
# **WalletPlatformAddOnPurchased**
> void WalletPlatformAddOnPurchased ()



An optional add-on product / service was just purchased.

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
    public class WalletPlatformAddOnPurchasedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.WalletPlatformAddOnPurchased();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.WalletPlatformAddOnPurchased: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalletPlatformAddOnPurchasedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.WalletPlatformAddOnPurchasedWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.WalletPlatformAddOnPurchasedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="walletplatforminvoicecreated"></a>
# **WalletPlatformInvoiceCreated**
> void WalletPlatformInvoiceCreated ()



A new invoice has been generated for your account.

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
    public class WalletPlatformInvoiceCreatedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.WalletPlatformInvoiceCreated();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.WalletPlatformInvoiceCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalletPlatformInvoiceCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.WalletPlatformInvoiceCreatedWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.WalletPlatformInvoiceCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="walletplatforminvoicepaid"></a>
# **WalletPlatformInvoicePaid**
> void WalletPlatformInvoicePaid ()



An invoice has just been paid for your account.

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
    public class WalletPlatformInvoicePaidExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.WalletPlatformInvoicePaid();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.WalletPlatformInvoicePaid: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalletPlatformInvoicePaidWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.WalletPlatformInvoicePaidWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.WalletPlatformInvoicePaidWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="walletplatformledgerentrycreated"></a>
# **WalletPlatformLedgerEntryCreated**
> void WalletPlatformLedgerEntryCreated (LedgerEntry? ledgerEntry = null)



A new ledger entry is created every time a redemption or refund event has occurred.

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
    public class WalletPlatformLedgerEntryCreatedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);
            var ledgerEntry = new LedgerEntry?(); // LedgerEntry? |  (optional) 

            try
            {
                apiInstance.WalletPlatformLedgerEntryCreated(ledgerEntry);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.WalletPlatformLedgerEntryCreated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalletPlatformLedgerEntryCreatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.WalletPlatformLedgerEntryCreatedWithHttpInfo(ledgerEntry);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.WalletPlatformLedgerEntryCreatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ledgerEntry** | [**LedgerEntry?**](LedgerEntry?.md) |  | [optional]  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="walletplatformpaymentmethodadded"></a>
# **WalletPlatformPaymentMethodAdded**
> void WalletPlatformPaymentMethodAdded ()



The payment method associated with your account has changed.

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
    public class WalletPlatformPaymentMethodAddedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.WalletPlatformPaymentMethodAdded();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.WalletPlatformPaymentMethodAdded: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalletPlatformPaymentMethodAddedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.WalletPlatformPaymentMethodAddedWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.WalletPlatformPaymentMethodAddedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="walletplatformsubscriptionchanged"></a>
# **WalletPlatformSubscriptionChanged**
> void WalletPlatformSubscriptionChanged ()



A change to your billing subscription has been made.

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
    public class WalletPlatformSubscriptionChangedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.wall.et";
            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new DefaultApi(httpClient, config, httpClientHandler);

            try
            {
                apiInstance.WalletPlatformSubscriptionChanged();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.WalletPlatformSubscriptionChanged: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalletPlatformSubscriptionChangedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.WalletPlatformSubscriptionChangedWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.WalletPlatformSubscriptionChangedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

