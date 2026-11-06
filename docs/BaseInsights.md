# BaseInsights

Base Insights for all insights which is used to extend insights for placement, keyword, searchterm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**has_next_page** | **bool** |  | [optional] 
**start_date** | **float** |  | [optional] 
**end_date** | **float** |  | [optional] 
**insights** | [**BaseInsightsInsights**](BaseInsightsInsights.md) |  | [optional] 

## Example

```python
from openapi_client.models.base_insights import BaseInsights

# TODO update the JSON string below
json = "{}"
# create an instance of BaseInsights from a JSON string
base_insights_instance = BaseInsights.from_json(json)
# print the JSON string representation of the object
print(BaseInsights.to_json())

# convert the object into a dict
base_insights_dict = base_insights_instance.to_dict()
# create an instance of BaseInsights from a dict
base_insights_from_dict = BaseInsights.from_dict(base_insights_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


