# FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200ResponseData


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
**rules** | **List[str]** | List of rule IDs associated with the campaign | [optional] 

## Example

```python
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get200_response_data import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200ResponseData from a JSON string
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get200_response_data_instance = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200ResponseData.from_json(json)
# print the JSON string representation of the object
print(FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200ResponseData.to_json())

# convert the object into a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get200_response_data_dict = flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get200_response_data_instance.to_dict()
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200ResponseData from a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get200_response_data_from_dict = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdGet200ResponseData.from_dict(flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_get200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


