# FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest


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
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest from a JSON string
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request_instance = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest.from_json(json)
# print the JSON string representation of the object
print(FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest.to_json())

# convert the object into a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request_dict = flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request_instance.to_dict()
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest from a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request_from_dict = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsPostRequest.from_dict(flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


