# FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique identifier for the object. | [optional] 
**budget** | **float** | Budget value. Either &#x60;budget&#x60; or &#x60;placements&#x60; or &#x60;targeting&#x60; must be provided. | [optional] 
**placements** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInnerPlacements**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInnerPlacements.md) |  | [optional] 
**targeting** | [**FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInnerTargeting**](FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInnerTargeting.md) |  | [optional] 

## Example

```python
from openapi_client.models.flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner import FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner

# TODO update the JSON string below
json = "{}"
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner from a JSON string
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner_instance = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner.from_json(json)
# print the JSON string representation of the object
print(FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner.to_json())

# convert the object into a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner_dict = flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner_instance.to_dict()
# create an instance of FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner from a dict
flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner_from_dict = FlipkartAdsBaBusinessAccountIdAaAdAccountIdCampaignsIdAdgroupsPatchRequestInner.from_dict(flipkart_ads_ba_business_account_id_aa_ad_account_id_campaigns_id_adgroups_patch_request_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


