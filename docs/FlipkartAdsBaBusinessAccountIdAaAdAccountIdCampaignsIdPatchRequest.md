# FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Campaign name | [optional] 
**start_date** | **float** | Campaign start date in epoch format | [optional] 
**end_date** | **float** | Campaign end date in epoch format | [optional] 
**budget** | **float** |  | [optional] 
**budget_type** | **str** | Campaign budget type only for brands for sellers its only TOTAL_BUDGET | [optional] 

## Example

```python
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest from a JSON string
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request_instance = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest.from_json(json)
# print the JSON string representation of the object
print(FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest.to_json())

# convert the object into a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request_dict = flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request_instance.to_dict()
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest from a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request_from_dict = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdPatchRequest.from_dict(flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


