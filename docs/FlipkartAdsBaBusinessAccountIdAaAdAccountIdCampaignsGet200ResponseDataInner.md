# FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique identifier for the campaign | [optional] 
**name** | **str** | Name of the campaign | [optional] 
**status** | **str** | Current status of the campaign | [optional] 
**budget_type** | **str** | Budget Type of campaign | [optional] 
**type** | **str** | Type of campaign | [optional] 
**start_date** | **float** |  | [optional] 
**end_date** | **float** |  | [optional] 
**budget** | **float** |  | [optional] 
**cost_model** | **str** |  | [optional] 
**metrics** | [**MetricsMetrics**](MetricsMetrics.md) |  | [optional] 

## Example

```python
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get200_response_data_inner import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200ResponseDataInner from a JSON string
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get200_response_data_inner_instance = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200ResponseDataInner.to_json())

# convert the object into a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get200_response_data_inner_dict = flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get200_response_data_inner_instance.to_dict()
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200ResponseDataInner from a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get200_response_data_inner_from_dict = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsGet200ResponseDataInner.from_dict(flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_get200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


