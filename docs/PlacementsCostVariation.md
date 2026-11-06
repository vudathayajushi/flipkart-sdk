# PlacementsCostVariation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**placements** | [**List[PlacementsCostVariationPlacementsInner]**](PlacementsCostVariationPlacementsInner.md) |  | [optional] 

## Example

```python
from openapi_client.models.placements_cost_variation import PlacementsCostVariation

# TODO update the JSON string below
json = "{}"
# create an instance of PlacementsCostVariation from a JSON string
placements_cost_variation_instance = PlacementsCostVariation.from_json(json)
# print the JSON string representation of the object
print(PlacementsCostVariation.to_json())

# convert the object into a dict
placements_cost_variation_dict = placements_cost_variation_instance.to_dict()
# create an instance of PlacementsCostVariation from a dict
placements_cost_variation_from_dict = PlacementsCostVariation.from_dict(placements_cost_variation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


