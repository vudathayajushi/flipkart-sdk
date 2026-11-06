# AdGroupPricing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique identifier for the ad group | [optional] 
**pricing_info** | [**AdGroupPricingAllOfPricingInfo**](AdGroupPricingAllOfPricingInfo.md) |  | [optional] 

## Example

```python
from openapi_client.models.ad_group_pricing import AdGroupPricing

# TODO update the JSON string below
json = "{}"
# create an instance of AdGroupPricing from a JSON string
ad_group_pricing_instance = AdGroupPricing.from_json(json)
# print the JSON string representation of the object
print(AdGroupPricing.to_json())

# convert the object into a dict
ad_group_pricing_dict = ad_group_pricing_instance.to_dict()
# create an instance of AdGroupPricing from a dict
ad_group_pricing_from_dict = AdGroupPricing.from_dict(ad_group_pricing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


