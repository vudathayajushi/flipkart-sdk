# openapi_client.BulkAPIsApi

All URIs are relative to *https://ads.api.flipkart.net*

Method | HTTP request | Description
------------- | ------------- | -------------
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_patch**](BulkAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/adgroups/bulk/status | Update status for multiple AdGroups IDs across Campaigns
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post**](BulkAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post) | **POST** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/adgroups/bulk/status | Get status for array of AdGroup IDs across Campaigns
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_banners_bulk_status_patch**](BulkAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_banners_bulk_status_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/banners/bulk/status | Update status for multiple Banner IDs across AdGroups and Campaigns
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch**](BulkAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/bulk/budget | Update the budget for multiple Campaign IDs and AdGroups (bannerGroup) within Campaigns
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post**](BulkAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post) | **POST** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/bulk/budget | Get Budgets for Campaign and AdGroups (bannerGroups) for array of Campaign IDs
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post**](BulkAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post) | **POST** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/bulk | Get all Campaign details for array of Campaign IDs
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch**](BulkAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/bulk/status | Update status for multiple Campaign IDs
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post**](BulkAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post) | **POST** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/bulk/status | Get status for array of Campaign IDs


# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_patch**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_patch(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update status for multiple AdGroups IDs across Campaigns

Update the status of multiple AdGroups (within an Ad Account – across all Campaigns of the Ad Account) by supplying the AdGroup IDs in a single request. (**NOTE**: This API can Update Statuses of **upto 50 AdGroups'** in a single API call)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest
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
    api_instance = openapi_client.BulkAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest | Payload to update status of entity (campaign / banner / adgroup)

    try:
        # Update status for multiple AdGroups IDs across Campaigns
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_patch(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request)
        print("The response of BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest.md)| Payload to update status of entity (campaign / banner / adgroup) | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | update adgroups status in bulk response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsAdgroupsBulkStatusPost200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get status for array of AdGroup IDs across Campaigns

Retrieve the current status (and uiStatus = status shown on the Ads Platform Campaign Manager) for multiple **AdGroups** (within an Ad Account, across all the Ad Campaigns in the Ad Account) in a single request. Supply the array of only AdGroup IDs in the Request Payload. (**NOTE**: This API can fetch **upto 100 AdGroups'** statuses in a single call)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsAdgroupsBulkStatusPost200Response
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest
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
    api_instance = openapi_client.BulkAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest | Payload to get details of multiple campaigns

    try:
        # Get status for array of AdGroup IDs across Campaigns
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request)
        print("The response of BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_adgroups_bulk_status_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest.md)| Payload to get details of multiple campaigns | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsAdgroupsBulkStatusPost200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsAdgroupsBulkStatusPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bulk Campaigns status response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_banners_bulk_status_patch**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_banners_bulk_status_patch(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_banners_bulk_status_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update status for multiple Banner IDs across AdGroups and Campaigns

Update the status of multiple BannerIDs (within an Ad Account – across all Campaigns and AdGroups of the Ad Account) by supplying the Banner IDs in a single request. (**NOTE**: This API can Update Statuses of **upto 50 Banners** in a single API call). 

**Important:** In order to PAUSE and RESUME Products (FSNs) in PLA Campaigns, you would need to interact with the Banner ID associated with that Product (each Banner ID is unique to an AdGroup x FSN combination) and using this PATCH API you can change the status of the Banner. The information needed for mapping of [Banner ID to FSN/Product ID] can be fetched from the first Bulk API in this table [the "Get all Campaign details..." API] 

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest
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
    api_instance = openapi_client.BulkAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest | Payload to update status of entity (campaign / banner / adgroup)

    try:
        # Update status for multiple Banner IDs across AdGroups and Campaigns
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_banners_bulk_status_patch(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request)
        print("The response of BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_banners_bulk_status_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_banners_bulk_status_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest.md)| Payload to update status of entity (campaign / banner / adgroup) | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | update banners status in bulk response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatch200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update the budget for multiple Campaign IDs and AdGroups (bannerGroup) within Campaigns

Update the Campaign budget for multiple Campaigns (within an Ad Account) along with the budgets for all AdGroups (bannerGroup) under each of the Campaigns in a single request. 
(**NOTE**: This API can update the budget of **maximum 10 Campaigns** – and corresponding AdGroup budgets – at a time, in a single API call)

**CAUTION:** 
 
(i) If you are looking to Update the Campaign Budgets alone, the new budget allotted to each of the Campaigns will be re-distributed among the AdGroups such that the new AdGroup budgets will be in the same proportion (w.r.t the Campaign Budget) as it was before the update, with the sum of the AdGroup budget automatically equalling the new Campaign Budget (necessary condition)

(ii) If you wish to update the AdGroup Budgets while updating the  Campaign Budgets, then you must **provide the new budget value for ALL the AdGroups within the Campaign** for which you are updating the budget, and **ensure that the sum of the AdGroup Budgets is adding up to the new total Campaign Budget you are setting** – with request payloads for Budget Update where the [Sum of AdGroup Budgets ≠  Campaign Budget], the API will throw an Error

(iii) If you receive a successfull response code 2xx, and a ≥0 "inProgressCount" value, it will be happenign to [budgeType = DAILY_BUDGET] Campaigns.
In order to geth the current status of these DAILY_BUDGET Campaign which are "inProgress" after updating their status:- you can use the first Bulk API in this table [the "Get all Campaign details..." API] to fetch thier current. status, i.e, thier status after the Budget change.

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatch200Response
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatchRequest
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
    api_instance = openapi_client.BulkAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatchRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatchRequest | Payload to update budget of entity (campaign / adgroup)

    try:
        # Update the budget for multiple Campaign IDs and AdGroups (bannerGroup) within Campaigns
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch_request)
        print("The response of BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_patch_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatchRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatchRequest.md)| Payload to update budget of entity (campaign / adgroup) | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatch200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bulk Campaigns status response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPost200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get Budgets for Campaign and AdGroups (bannerGroups) for array of Campaign IDs

Get the Campaign budget for multiple Campaigns (within an Ad Account) along with the budgets for all AdGroups (bannerGroup) under each of the Campaigns in a single request. Supply the array of Campaign IDs in the Request Payload. (**NOTE**: This API can fetch **upto 100 Campaigns'** – and corresponding AdGroups' – Budgets in a single API call)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPost200Response
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest
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
    api_instance = openapi_client.BulkAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest | Payload to get details of multiple campaigns

    try:
        # Get Budgets for Campaign and AdGroups (bannerGroups) for array of Campaign IDs
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request)
        print("The response of BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_budget_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest.md)| Payload to get details of multiple campaigns | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPost200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkBudgetPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bulk Campaigns status response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post**
> BulkCampaigns flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get all Campaign details for array of Campaign IDs

Retrieve the Campaign configuration details for multiple Campaigns (within an Ad Account) in a single request. Supply the array of Campaign IDs in the Request Payload. (**NOTE**: Please supply **less than 20 Campaign IDs** in one API call at a time)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.bulk_campaigns import BulkCampaigns
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest
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
    api_instance = openapi_client.BulkAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest | Payload to get details of multiple campaigns

    try:
        # Get all Campaign details for array of Campaign IDs
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request)
        print("The response of BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest.md)| Payload to get details of multiple campaigns | 

### Return type

[**BulkCampaigns**](BulkCampaigns.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bulk Campaigns response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update status for multiple Campaign IDs

Update the status of multiple Campaigns (within an Ad Account) by supplying the Campaign IDs in a single request.  (**NOTE**: This API can Update Statuses of **upto 50 Campaigns'** in a single API call)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest
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
    api_instance = openapi_client.BulkAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest | Payload to update status of entity (campaign / banner / adgroup)

    try:
        # Update status for multiple Campaign IDs
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request)
        print("The response of BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatchRequest.md)| Payload to update status of entity (campaign / banner / adgroup) | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bulk Campaigns update status response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPost200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get status for array of Campaign IDs

Retrieve the current status (and uiStatus = status shown on the Ads Platform Campaign Manager) for multiple Campaigns (within an Ad Account) in a single request. Supply the array of Campaign IDs in the Request Payload. (**NOTE**: This API can fetch **upto 100 Campaigns'** statuses in a single call)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPost200Response
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
    api_instance = openapi_client.BulkAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest | Payload to get details of multiple campaigns

    try:
        # Get status for array of Campaign IDs
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post(business_account_id, ad_account_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request)
        print("The response of BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BulkAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_post_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkPostRequest.md)| Payload to get details of multiple campaigns | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPost200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bulk Campaigns status response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

