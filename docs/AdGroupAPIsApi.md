# openapi_client.AdGroupAPIsApi

All URIs are relative to *https://ads.api.flipkart.net*

Method | HTTP request | Description
------------- | ------------- | -------------
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_adgroup_id_actions_patch**](AdGroupAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_adgroup_id_actions_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id}/adgroups/{adgroup_id}/actions | Update Ad Groups Status given an AdGroup ID
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch**](AdGroupAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id}/adgroups/banner/{banner_id}/actions | Update Banner Status within AdGroups given a Campaign ID
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_get**](AdGroupAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id}/adgroups | Get configuration of Ad Groups within a Campaign given a Campaign ID
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch**](AdGroupAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch) | **PATCH** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id}/adgroups | Update/Modify (multiple) AdGroup parameters given a Campaign ID
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post**](AdGroupAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post) | **POST** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id}/adgroups | Create Ad Groups within a specific Campaign given a Campaign ID
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_pricing_get**](AdGroupAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_pricing_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/campaigns/{id}/adgroups/pricing | Get Pricing (Bidding) information for all AdGroups given a Campaign ID


# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_adgroup_id_actions_patch**
> GenericSuccess flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_adgroup_id_actions_patch(business_account_id, ad_account_id, id, adgroup_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_adgroup_id_actions_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update Ad Groups Status given an AdGroup ID

Update the status of the AdGroup within a specific Campaign. This API can be used change the Status of any single AdGroup within a Campaign to [LIVE/PAUSE/ABORT] from its previous state.

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
    api_instance = openapi_client.AdGroupAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID
    adgroup_id = 'adgroup_id_example' # str | Adgroup ID
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdActionsPatchRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdActionsPatchRequest | Payload to update status of entity (campaign / adgroup )

    try:
        # Update Ad Groups Status given an AdGroup ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_adgroup_id_actions_patch(business_account_id, ad_account_id, id, adgroup_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_actions_patch_request)
        print("The response of AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_adgroup_id_actions_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_adgroup_id_actions_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 
 **adgroup_id** | **str**| Adgroup ID | 
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

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch**
> GenericSuccess flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch(business_account_id, ad_account_id, id, banner_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update Banner Status within AdGroups given a Campaign ID

Update the status of any Banner which is available within the AdGroups of a specified Campaign ID.
This API can be used change the Status of any Banner (i.e, the Product within an AdGroup) within a Campaign to [LIVE/PAUSE] from its previous state.

**Note:**

i) For PLA Campaigns and AdGroups, each unique product within an AdGroup is assigned a unique Banner ID, which can be used in this API to update the status of that particular product in the AdGroup (since this API takes Banner ID as an Input)

ii) It is advisable to save the [Banner ID x product ID (fsn) mapping] for all concerned Campaigns in your system to ensure you can directly call this API when the PAUSE/LIVE action for any product has to be taken


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsBannerBannerIdActionsPatchRequest
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
    api_instance = openapi_client.AdGroupAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID
    banner_id = 'banner_id_example' # str | Banner ID
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsBannerBannerIdActionsPatchRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsBannerBannerIdActionsPatchRequest | Payload to update status of entity (banner)

    try:
        # Update Banner Status within AdGroups given a Campaign ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch(business_account_id, ad_account_id, id, banner_id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch_request)
        print("The response of AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 
 **banner_id** | **str**| Banner ID | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_banner_banner_id_actions_patch_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsBannerBannerIdActionsPatchRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsBannerBannerIdActionsPatchRequest.md)| Payload to update status of entity (banner) | 

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

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_get**
> AdGroup flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_get(business_account_id, ad_account_id, id)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get configuration of Ad Groups within a Campaign given a Campaign ID

Get set of all AdGroups within a Campaign, along with their current configurations and entities (such as Bids, Keywords, Banner IDs, Products, etc.)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.ad_group import AdGroup
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
    api_instance = openapi_client.AdGroupAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID

    try:
        # Get configuration of Ad Groups within a Campaign given a Campaign ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_get(business_account_id, ad_account_id, id)
        print("The response of AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 

### Return type

[**AdGroup**](AdGroup.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Campaign response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch**
> AdGroup flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch(business_account_id, ad_account_id, id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Update/Modify (multiple) AdGroup parameters given a Campaign ID

Update the configuration parameters of a MULTIPLE AdGroups given a Campaign ID. (using this API, you can provide one or more fields in the request payload, that can be update)

**Note:**

i) If the Campaign is running, then specifically within the AdGroup, the only mutable parameters using this API are Placement Bids and Keywords

ii) Individual Placement Bids can be provided (not all Bids need to be provided) for the Update API to change the bids

iii) Within the indiviudal Keyword arrays ("include", "exclude"), if they are used in this PATCH Update AdGroup API, they will ALWYAS OVERWRITE the EXISTING KEYWORDs  (for.eg, if you already had 10 keywords in "include" array of the Keywords, and you wanted to add 10 more keywords, then you have to supply a payload with 20 total keywords for the API to update them for this AdGroup)

iv) In case of ROI (Smart ROI) campaign only cost and exclude keywords is available, placement and include keywords is not supported


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.ad_group import AdGroup
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner
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
    api_instance = openapi_client.AdGroupAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner = [openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner()] # List[FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner] | **⚠️ CAUTION:**   1. If this API is used to Update the \"Search_Page\" Bids or the \"targeting\" Struct for a Campaign which has Keyword Bidding Enabled, then the Bids allocated to the placement \"Search_Page\" will override the Bids for each Keyword which were assigned in Keyword Bidding Page. 2. In order to Update the Keywords in this API, you must supply the full list of new Keyword that you want you AdGroup to target at (for. eg, if there were 10 keywords in the AdGroup, and you wanted to add 10 new keywords, then you will have to supply a list of 20 Keywords). Hence, it is advisable to store the Keywords for each campaign once it is fetched, or you can call any of the APIs which fetch you AdGroup details. 

    try:
        # Update/Modify (multiple) AdGroup parameters given a Campaign ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch(business_account_id, ad_account_id, id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner)
        print("The response of AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner** | [**List[FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner]**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner.md)| **⚠️ CAUTION:**   1. If this API is used to Update the \&quot;Search_Page\&quot; Bids or the \&quot;targeting\&quot; Struct for a Campaign which has Keyword Bidding Enabled, then the Bids allocated to the placement \&quot;Search_Page\&quot; will override the Bids for each Keyword which were assigned in Keyword Bidding Page. 2. In order to Update the Keywords in this API, you must supply the full list of new Keyword that you want you AdGroup to target at (for. eg, if there were 10 keywords in the AdGroup, and you wanted to add 10 new keywords, then you will have to supply a list of 20 Keywords). Hence, it is advisable to store the Keywords for each campaign once it is fetched, or you can call any of the APIs which fetch you AdGroup details.  | 

### Return type

[**AdGroup**](AdGroup.md)

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

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post**
> AdGroup flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post(business_account_id, ad_account_id, id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post_request)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Create Ad Groups within a specific Campaign given a Campaign ID

Create multiple AdGroups within a single Campaign by supplying a list of productIDs that you want to run the Ad Campaign for.

**Note:**

i) For PLA Campaigns, AdGroups are system generated based on the categorization of products

ii) The response will give the AdGroups created (based on input products) and the default configurations parameter values for each AdGroup

iii) Each unique product within an AdGroup is assigned a unique Banner ID, which can later be used to update the status of that particular product in the AdGroup


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.ad_group import AdGroup
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPostRequest
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
    api_instance = openapi_client.AdGroupAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID
    flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post_request = openapi_client.FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPostRequest() # FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPostRequest | Payload to create ad groups

    try:
        # Create Ad Groups within a specific Campaign given a Campaign ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post(business_account_id, ad_account_id, id, flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post_request)
        print("The response of AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 
 **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_post_request** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPostRequest**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPostRequest.md)| Payload to create ad groups | 

### Return type

[**AdGroup**](AdGroup.md)

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

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_pricing_get**
> AdGroupPricing flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_pricing_get(business_account_id, ad_account_id, id)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_pricing_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get Pricing (Bidding) information for all AdGroups given a Campaign ID

Get the Pricing (Bidding) informations for a set of AdGroups within a specific Campaign ID. Each AdGroup will have a set of its own Bidding related info, which can be used while adding Placement Bids in the PATCH AdGroup API.

**Note:**

i) "indicativePrice" is the minimum bid that applied for any Placement within the AdGroup

ii) "ceilingPrice" is the maximum amount you can bid for any Placement within the AdGroup

iii) "winningAvgCpx" to "winningMaxCpx" is the recommended range for bids that can be applied for a given category of products corresponding to the specific AdGroups


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.ad_group_pricing import AdGroupPricing
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
    api_instance = openapi_client.AdGroupAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    id = 'id_example' # str | Campaign ID

    try:
        # Get Pricing (Bidding) information for all AdGroups given a Campaign ID
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_pricing_get(business_account_id, ad_account_id, id)
        print("The response of AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_pricing_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdGroupAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_pricing_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **id** | **str**| Campaign ID | 

### Return type

[**AdGroupPricing**](AdGroupPricing.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Campaign response |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

