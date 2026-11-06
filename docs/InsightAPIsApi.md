# openapi_client.InsightAPIsApi

All URIs are relative to *https://ads.api.flipkart.net*

Method | HTTP request | Description
------------- | ------------- | -------------
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get**](InsightAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/insights | Retrieve Campaign performance metrics at different Granularities


# **flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdInsightsGet200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get(business_account_id, ad_account_id, start_date, end_date, type, ad_product, page_size=page_size, page_number=page_number, group_by_date=group_by_date, marketplace=marketplace)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Retrieve Campaign performance metrics at different Granularities

For PLA: Get PLACEMENT / KEYWORD / SEARCHTEM insights/reports for all PLA Campaigns within an Ad Account

For PCA: Get PLACEMENT / KEYWORD / SEARCHTEM / ATTRIBUTED_FSN insights/reports for all PCA Campaigns within an Ad Account

**Note:** -

i) This is a paginated API, you would have to keep calling the API for each page; the count of total pages will be present in each API call Response

ii) For fetching the data, you need to specify the startDate and endDate (maximum of 90days of Data can be fetched at a time, 365 days of lookback to fetch data is available)

iii) The latency in data for this API is 6 - 11 hours (metrics such as clicks, spends will update faster as compared to revenue, units, which could take upto 11 hrs too)"

iv) Please refer to PLA Insights Table and PCA Insights Table in [Entities](https://advertising.flipkart.com/swagger-docs/api/reference/entities/) for the description for each of the fields and metrics


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdInsightsGet200Response
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://ads.api.flipkart.net
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://ads.api.flipkart.net"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
async with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.InsightAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    start_date = 3.4 # float | Start date for the data. **Use IST (Indian Standard Time) timestamp based Unix Epoch format.**
    end_date = 3.4 # float | End date for the data. **Use IST (Indian Standard Time) timestamp based Unix Epoch format.**
    type = 'type_example' # str | Type of insights data to retrieve
    ad_product = 'ad_product_example' # str | adProduct = 'PLA' for fetching PLA Campaigns' data <br> adProduct = 'PCA' for fetching PCA Campaigns' data 
    page_size = 20 # int | Number of elements to return (Max Limit: 500) (optional) (default to 20)
    page_number = 1 # int | Page number to start the result (optional) (default to 1)
    group_by_date = False # bool | Optional flag to group the response data by date. (optional) (default to False)
    marketplace = 'FLIPKART' # str | Optional marketplace filter for insights data.  Supported only for the following **adProduct** and **type** combinations: - **PLA + PLACEMENT** (Advertising Portal / Brand ad accounts only) - **PLA + KEYWORD** or **PLA + SEARCHTERM** (Advertising Portal and SellerHub ad accounts) - **PCA + PLACEMENT** or **PCA + ATTRIBUTED_FSN** (Advertising Portal and SellerHub ad accounts)  (optional) (default to 'FLIPKART')

    try:
        # Retrieve Campaign performance metrics at different Granularities
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get(business_account_id, ad_account_id, start_date, end_date, type, ad_product, page_size=page_size, page_number=page_number, group_by_date=group_by_date, marketplace=marketplace)
        print("The response of InsightAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InsightAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_insights_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **start_date** | **float**| Start date for the data. **Use IST (Indian Standard Time) timestamp based Unix Epoch format.** | 
 **end_date** | **float**| End date for the data. **Use IST (Indian Standard Time) timestamp based Unix Epoch format.** | 
 **type** | **str**| Type of insights data to retrieve | 
 **ad_product** | **str**| adProduct &#x3D; &#39;PLA&#39; for fetching PLA Campaigns&#39; data &lt;br&gt; adProduct &#x3D; &#39;PCA&#39; for fetching PCA Campaigns&#39; data  | 
 **page_size** | **int**| Number of elements to return (Max Limit: 500) | [optional] [default to 20]
 **page_number** | **int**| Page number to start the result | [optional] [default to 1]
 **group_by_date** | **bool**| Optional flag to group the response data by date. | [optional] [default to False]
 **marketplace** | **str**| Optional marketplace filter for insights data.  Supported only for the following **adProduct** and **type** combinations: - **PLA + PLACEMENT** (Advertising Portal / Brand ad accounts only) - **PLA + KEYWORD** or **PLA + SEARCHTERM** (Advertising Portal and SellerHub ad accounts) - **PCA + PLACEMENT** or **PCA + ATTRIBUTED_FSN** (Advertising Portal and SellerHub ad accounts)  | [optional] [default to &#39;FLIPKART&#39;]

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdInsightsGet200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdInsightsGet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | insights at ad account level for placement, keyword, searchterm |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

