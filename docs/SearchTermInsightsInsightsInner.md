# SearchTermInsightsInsightsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metrics** | [**MetricsMetrics**](MetricsMetrics.md) |  | [optional] 
**augmented_query** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.search_term_insights_insights_inner import SearchTermInsightsInsightsInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchTermInsightsInsightsInner from a JSON string
search_term_insights_insights_inner_instance = SearchTermInsightsInsightsInner.from_json(json)
# print the JSON string representation of the object
print(SearchTermInsightsInsightsInner.to_json())

# convert the object into a dict
search_term_insights_insights_inner_dict = search_term_insights_insights_inner_instance.to_dict()
# create an instance of SearchTermInsightsInsightsInner from a dict
search_term_insights_insights_inner_from_dict = SearchTermInsightsInsightsInner.from_dict(search_term_insights_insights_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


