# AdGroupBulk


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique identifier for the ad group | [optional] 
**name** | **str** | Name of the ad group | [optional] 
**status** | **str** |  | [optional] 
**ui_status** | **str** |  | [optional] 
**product_count** | **float** |  | [optional] 
**commodity_id** | **float** |  | [optional] 
**cost_model** | **str** |  | [optional] 
**cost** | **float** |  | [optional] 
**budget** | **float** |  | [optional] 
**budget_type** | **str** | Budget Type of adgroup | [optional] 
**banners** | [**List[AdGroupBaseBannersInner]**](AdGroupBaseBannersInner.md) |  | [optional] 
**store_paths** | **List[str]** |  | [optional] 
**targeting** | [**TargetingTargeting**](TargetingTargeting.md) |  | [optional] 
**cost_variation** | [**PlacementsCostVariation**](PlacementsCostVariation.md) |  | [optional] 

## Example

```python
from openapi_client.models.ad_group_bulk import AdGroupBulk

# TODO update the JSON string below
json = "{}"
# create an instance of AdGroupBulk from a JSON string
ad_group_bulk_instance = AdGroupBulk.from_json(json)
# print the JSON string representation of the object
print(AdGroupBulk.to_json())

# convert the object into a dict
ad_group_bulk_dict = ad_group_bulk_instance.to_dict()
# create an instance of AdGroupBulk from a dict
ad_group_bulk_from_dict = AdGroupBulk.from_dict(ad_group_bulk_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


