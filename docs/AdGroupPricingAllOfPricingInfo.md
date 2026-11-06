# AdGroupPricingAllOfPricingInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**commodity_id** | **float** |  | [optional] 
**pricing_info** | [**AdGroupPricingAllOfPricingInfoPricingInfo**](AdGroupPricingAllOfPricingInfoPricingInfo.md) |  | [optional] 
**winning_bid_range** | [**AdGroupPricingAllOfPricingInfoWinningBidRange**](AdGroupPricingAllOfPricingInfoWinningBidRange.md) |  | [optional] 

## Example

```python
from openapi_client.models.ad_group_pricing_all_of_pricing_info import AdGroupPricingAllOfPricingInfo

# TODO update the JSON string below
json = "{}"
# create an instance of AdGroupPricingAllOfPricingInfo from a JSON string
ad_group_pricing_all_of_pricing_info_instance = AdGroupPricingAllOfPricingInfo.from_json(json)
# print the JSON string representation of the object
print(AdGroupPricingAllOfPricingInfo.to_json())

# convert the object into a dict
ad_group_pricing_all_of_pricing_info_dict = ad_group_pricing_all_of_pricing_info_instance.to_dict()
# create an instance of AdGroupPricingAllOfPricingInfo from a dict
ad_group_pricing_all_of_pricing_info_from_dict = AdGroupPricingAllOfPricingInfo.from_dict(ad_group_pricing_all_of_pricing_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


