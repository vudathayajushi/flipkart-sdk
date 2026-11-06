# openapi_client.AccountAPIsApi

All URIs are relative to *https://ads.api.flipkart.net*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ads_v1_users_authorised_accounts_get**](AccountAPIsApi.md#ads_v1_users_authorised_accounts_get) | **GET** /ads/v1/users/authorised_accounts | Get the Accounts accessible by a single Bearer Token (Deprecated)
[**ads_v3_users_authorised_accounts_get**](AccountAPIsApi.md#ads_v3_users_authorised_accounts_get) | **GET** /ads/v3/users/authorised_accounts | Get the Accounts accessible by a single Bearer Token
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_brands_get**](AccountAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_brands_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/brands | Get the available Brands for a specific Ad Account
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get**](AccountAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/costModels | Get the available CostModels for a specific Ad Account
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_marketplace_get**](AccountAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_marketplace_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/marketplace | Get the available Marketplace for a specific Ad Account
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get**](AccountAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/products | Get the available Products Catalog Info for a specific Ad Account
[**flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get**](AccountAPIsApi.md#flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get) | **GET** /flipkart-ads/ba/{business_account_id}/aa/{ad_account_id}/stores | Get the available Stores for a specific Ad Account


# **ads_v1_users_authorised_accounts_get**
> List[str] ads_v1_users_authorised_accounts_get()

**Synchronous variant:** `ads_v1_users_authorised_accounts_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get the Accounts accessible by a single Bearer Token (Deprecated)

**Deprecated:** Use `GET /ads/v3/users/authorised_accounts` instead.

Get the list of Business Accounts and Ad Accounts that are accessible for a given OAuth (Bearer) token generated.


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
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
    api_instance = openapi_client.AccountAPIsApi(api_client)

    try:
        # Get the Accounts accessible by a single Bearer Token (Deprecated)
        api_response = await api_instance.ads_v1_users_authorised_accounts_get()
        print("The response of AccountAPIsApi->ads_v1_users_authorised_accounts_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountAPIsApi->ads_v1_users_authorised_accounts_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**List[str]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | business accounts |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ads_v3_users_authorised_accounts_get**
> AuthorisedAccountsResponse ads_v3_users_authorised_accounts_get()

**Synchronous variant:** `ads_v3_users_authorised_accounts_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get the Accounts accessible by a single Bearer Token

Get the list of ad accounts accessible for a given OAuth (Bearer) token. Returns a map of account IDs to account details. Seller tokens return a single seller ad account; brand/agency tokens may return multiple brand ad accounts.

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.authorised_accounts_response import AuthorisedAccountsResponse
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
    api_instance = openapi_client.AccountAPIsApi(api_client)

    try:
        # Get the Accounts accessible by a single Bearer Token
        api_response = await api_instance.ads_v3_users_authorised_accounts_get()
        print("The response of AccountAPIsApi->ads_v3_users_authorised_accounts_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountAPIsApi->ads_v3_users_authorised_accounts_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AuthorisedAccountsResponse**](AuthorisedAccountsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Authorised accounts accessible by the bearer token |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_brands_get**
> List[str] flipkart_ads_ba_business_account_id_aa_ad_account_id_brands_get(business_account_id, ad_account_id)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_brands_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get the available Brands for a specific Ad Account

Get the list of available Brands of the products for which Ads can be created for a given Ad Account.

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
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
    api_instance = openapi_client.AccountAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account

    try:
        # Get the available Brands for a specific Ad Account
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_brands_get(business_account_id, ad_account_id)
        print("The response of AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_brands_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_brands_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 

### Return type

**List[str]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | brands available at account level |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get**
> List[FlipkartAdsBaBusinessAccountIdAaAdAccountIdCostModelsGet200ResponseInner] flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get(business_account_id, ad_account_id)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get the available CostModels for a specific Ad Account

Get the list of available CostModels for a given Ad Account.
Currently, only 2 CostModels are used for PLA/PCA Ad Campaigns, CPC (Cost-Per-Click) and ROI (sROI or Smart ROI)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get200_response_inner import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCostModelsGet200ResponseInner
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
    api_instance = openapi_client.AccountAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account

    try:
        # Get the available CostModels for a specific Ad Account
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get(business_account_id, ad_account_id)
        print("The response of AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_cost_models_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 

### Return type

[**List[FlipkartAdsBaBusinessAccountIdAaAdAccountIdCostModelsGet200ResponseInner]**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCostModelsGet200ResponseInner.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | costmodel available at account level |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_marketplace_get**
> List[str] flipkart_ads_ba_business_account_id_aa_ad_account_id_marketplace_get(business_account_id, ad_account_id)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_marketplace_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get the available Marketplace for a specific Ad Account

Get the list of Marketplaces available to access for a given Ad Account.

[**Note:** Currently, only FLIPKART marketplace is active for ALL APIs]


### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
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
    api_instance = openapi_client.AccountAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account

    try:
        # Get the available Marketplace for a specific Ad Account
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_marketplace_get(business_account_id, ad_account_id)
        print("The response of AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_marketplace_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_marketplace_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 

### Return type

**List[str]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | marketplace available at account level |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdProductsGet200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get(business_account_id, ad_account_id, category, brand_ids, page=page, limit=limit)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get the available Products Catalog Info for a specific Ad Account

Get the list of available Products (with unique FSN IDs, where FSN = Flipkart Serial Number, a unique identifier for each product in Flipkart).
[**Note:** Additional information such as Product title and Product Image (as displayed on Flipkart), Brand, Stores, and Price range are also available in the response – this can be used to render interactive Product tiles on any platform to enable a User Inerface for selecting products to advertise]

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdProductsGet200Response
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
    api_instance = openapi_client.AccountAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account
    category = 'category_example' # str | store path
    brand_ids = ['brand_ids_example'] # List[str] | brand id
    page = 56 # int | page number (optional)
    limit = 56 # int | page size (optional)

    try:
        # Get the available Products Catalog Info for a specific Ad Account
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get(business_account_id, ad_account_id, category, brand_ids, page=page, limit=limit)
        print("The response of AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_products_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 
 **category** | **str**| store path | 
 **brand_ids** | [**List[str]**](str.md)| brand id | 
 **page** | **int**| page number | [optional] 
 **limit** | **int**| page size | [optional] 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdProductsGet200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdProductsGet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | products available at account level |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get**
> FlipkartAdsBaBusinessAccountIdAaAdAccountIdStoresGet200Response flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get(business_account_id, ad_account_id)

**Synchronous variant:** `flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get_sync(...)` — same parameters and return type, but blocks until completion instead of requiring `await`.

Get the available Stores for a specific Ad Account

Get the list of available Stores (i.e, Categories) for which Ads can be created for a given Ad Account.
[**Note:** 'storeTitle' shown in the response is the same as the 'Category Name' used on the Advertising Portal)

### Example

* Bearer (JWT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get200_response import FlipkartAdsBaBusinessAccountIdAaAdAccountIdStoresGet200Response
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
    api_instance = openapi_client.AccountAPIsApi(api_client)
    business_account_id = 'business_account_id_example' # str | ID of the business account
    ad_account_id = 'ad_account_id_example' # str | ID of the advertising account

    try:
        # Get the available Stores for a specific Ad Account
        api_response = await api_instance.flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get(business_account_id, ad_account_id)
        print("The response of AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountAPIsApi->flipkart_ads_ba_business_account_id_aa_ad_account_id_stores_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **business_account_id** | **str**| ID of the business account | 
 **ad_account_id** | **str**| ID of the advertising account | 

### Return type

[**FlipkartAdsBaBusinessAccountIdAaAdAccountIdStoresGet200Response**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdStoresGet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | stores available at account level |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

