# PlacementFSNInsightsInsightsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metrics** | [**MetricsMetrics**](MetricsMetrics.md) |  | [optional] 
**product_id** | **str** |  | [optional] 
**product_name** | **str** |  | [optional] 
**converted_fsn** | **str** |  | [optional] 
**placement_type** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.placement_fsn_insights_insights_inner import PlacementFSNInsightsInsightsInner

# TODO update the JSON string below
json = "{}"
# create an instance of PlacementFSNInsightsInsightsInner from a JSON string
placement_fsn_insights_insights_inner_instance = PlacementFSNInsightsInsightsInner.from_json(json)
# print the JSON string representation of the object
print(PlacementFSNInsightsInsightsInner.to_json())

# convert the object into a dict
placement_fsn_insights_insights_inner_dict = placement_fsn_insights_insights_inner_instance.to_dict()
# create an instance of PlacementFSNInsightsInsightsInner from a dict
placement_fsn_insights_insights_inner_from_dict = PlacementFSNInsightsInsightsInner.from_dict(placement_fsn_insights_insights_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


