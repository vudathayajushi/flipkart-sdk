# FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | [**List[FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseDataSuccessInner]**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseDataSuccessInner.md) |  | [optional] 
**failed** | [**List[FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseDataFailedInner]**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseDataFailedInner.md) |  | [optional] 
**in_progress_count** | **int** |  | [optional] 

## Example

```python
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response_data import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseData from a JSON string
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response_data_instance = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseData.from_json(json)
# print the JSON string representation of the object
print(FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseData.to_json())

# convert the object into a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response_data_dict = flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response_data_instance.to_dict()
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseData from a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response_data_from_dict = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsBulkStatusPatch200ResponseData.from_dict(flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_bulk_status_patch200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


