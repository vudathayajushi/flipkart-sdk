# openapi_client.CampaignAPIsApi

All URIs are relative to *https://ads.api.flipkart.net*

Method | HTTP request | Description
------------- | ------------- | -------------
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get**](CampaignAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns | Retrieve the list of Campaigns with configuration and Metrics given an Ad Account
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch**](CampaignAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id}/actions | Update the Status of the Campaign given a Campaign ID
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get**](CampaignAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id} | Get Campaign details given a Campaign ID
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch**](CampaignAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id} | Update/Modify the campaign parameters given a Campaign ID
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post**](CampaignAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post) | **POST** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns | Create a Draft Campaign in a specific Ad account


# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get(business_account_id, ad_account_id, start_date, end_date, ad_product, page_size=page_size, page_number=page_number, group_by_date=group_by_date)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Retrieve the list of Campaigns with configuration and Metrics given an Ad Account

"Get the list of all Campaign IDs within a given Ad Account, alongwith the configuration parameters of the Ad Campaign as well as the performance Metrics of the Ad Campaign, for a time period between a specified startDate and endDate

**Note:**

i) This is a paginated API, you would have to keep calling the API for each page, as long as you have fetched the campaigns for given count.

ii) For fetching the data, you need to specify the startDate and endDate (maximum of 90days of Data can be fetched at a time, 365 days of lookback to fetch data is available)

iii) The latency in data for this API is 3 - 5 hours (metrics such as clicks, spends will update faster as compared to revenue, units, which could take upto 11 hrs too)"

iv) Please refer to Campaign Table in [Entities](https://advertising.flipkart.com/swagger-docs/api/reference/entities/) for the description for each of the fields and metrics


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200Response
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
    api_instance = openapi_client.CampaignAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    start_date = 3.4 # float | Start date for the data. **Use IST (Indian Standard Time) timestamp based Unix Epoch format.**
    end_date = 3.4 # float | End date for the data. **Use IST (Indian Standard Time) timestamp based Unix Epoch format.**
    ad_product = ['ad_product_example'] # List[str] | adProduct[]=PLA for fetching PLA Campaigns' data <br> adProduct[]=PCA for fetching PCA Campaigns' data <br> adProduct[]=[PLA,PCA] for fetching data for both PLA and PCA Campaigns' data  
    page_size = 20 # int | Number of elements to return (Max Limit: 400) (optional) (default to 20)
    page_number = 1 # int | Page number to start the result (optional) (default to 1)
    group_by_date = False # bool | Optional flag to group the response data by date. (optional) (default to False)

    try:
        # Retrieve the list of Campaigns with configuration and Metrics given an Ad Account
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get(business_account_id, ad_account_id, start_date, end_date, ad_product, page_size=page_size, page_number=page_number, group_by_date=group_by_date)
        print("The response of CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **start_date** | **float**| Start date for the data. **Use IST (Indian Standard Time) timestamp based Unix Epoch format.** | 
 **end_date** | **float**| End date for the data. **Use IST (Indian Standard Time) timestamp based Unix Epoch format.** | 
 **ad_product** | [**List[str]**](str.md)| adProduct[]&#x3D;PLA for fetching PLA Campaigns&#39; data &lt;br&gt; adProduct[]&#x3D;PCA for fetching PCA Campaigns&#39; data &lt;br&gt; adProduct[]&#x3D;[PLA,PCA] for fetching data for both PLA and PCA Campaigns&#39; data   | 
 **page_size** | **int**| Number of elements to return (Max Limit: 400) | [optional] [default to 20]
 **page_number** | **int**| Page number to start the result | [optional] [default to 1]
 **group_by_date** | **bool**| Optional flag to group the response data by date. | [optional] [default to False]

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of campaigns under the adaccount |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch**
> GenericSuccess flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch(business_account_id, ad_account_id, id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update the Status of the Campaign given a Campaign ID

Update Campaign status of any Campaign within the Ad account; this API is used to change the state of a Campaign (LIVE/PAUSE) from its previous state.

[**Note:** After Creation of a Draft campaign, you need to use this API (or the Bulk Campaign Status API) to make the Campaign LIVE for it to start consuming budget and showing Ads on Flipkart]

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdActionsPatchRequest
from openapi_client.models.generic_success import GenericSuccess
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
    api_instance = openapi_client.CampaignAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdActionsPatchRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdActionsPatchRequest | Payload to update status of entity (campaign / adgroup )

    try:
        # Update the Status of the Campaign given a Campaign ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch(business_account_id, ad_account_id, id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_request)
        print("The response of CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdActionsPatchRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdActionsPatchRequest.md)| Payload to update status of entity (campaign / adgroup ) | 

### Return type

[**GenericSuccess**](GenericSuccess.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Action response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get(business_account_id, ad_account_id, id)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get Campaign details given a Campaign ID

Retrieve the configruation details of a specific Campaign given a Campaign ID.

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200Response
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
    api_instance = openapi_client.CampaignAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID

    try:
        # Get Campaign details given a Campaign ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get(business_account_id, ad_account_id, id)
        print("The response of CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Campaign details |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatch200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch(business_account_id, ad_account_id, id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update/Modify the campaign parameters given a Campaign ID

Update the configuration parameters of a specific campaign given a campaign ID. (using this API, you can provide one or more fields in the request payload, that can be update)

**Note:**

i) Once a Campaign is running, only mutable parameters, such as Budget, Status, endDate,etc. can be updated – similar to what is allowed on the advertising portal

ii) If update the budget of a Campaign, the new budget allotted to the Campaign will be re-distributed among the AdGroups such that the new AdGroup budgets will be in the same proportion (w.r.t the new Campaign Budget) as it was before the update, with the sum of the AdGroup budget automatically equalling the new Campaign Budget (necessary condition enforced by the system)

iii) If you are trying to add products to a Campaign which is in a "Draft" state (not made live yet) then the list of products you are adding will over-ride the already existing Adgroups. If the campaign is in the live state, then the new product will get added to an existing AdGroup within the campaigns or form a new AdGroup


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatch200Response
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest
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
    api_instance = openapi_client.CampaignAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest | Payload to update a campaign (either one of the fields can be provided for update)

    try:
        # Update/Modify the campaign parameters given a Campaign ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch(business_account_id, ad_account_id, id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request)
        print("The response of CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest.md)| Payload to update a campaign (either one of the fields can be provided for update) | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatch200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated Campaign details |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post**
> Campaign flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Create a Draft Campaign in a specific Ad account

Create a Draft Ad Campaign with specified parameters in a given Ad account. This will create the Campaign ID for this entity with the parameter values provided.

[**Note:** This Draft campaign will NOT run and serve Ads on Flipkart Platform untill it is made LIVE – which can be done by Updating the Campaign Status]

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.campaign import Campaign
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest
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
    api_instance = openapi_client.CampaignAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest | Payload to create a draft campaign (only required fields is needed rest will be created with default value)

    try:
        # Create a Draft Campaign in a specific Ad account
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request)
        print("The response of CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest.md)| Payload to create a draft campaign (only required fields is needed rest will be created with default value) | 

### Return type

[**Campaign**](Campaign.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Campaign response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

