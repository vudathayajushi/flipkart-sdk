# SearchTermInsights

Insights for search term at adgroup level for account

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**insights** | [**List[SearchTermInsightsInsightsInner]**](SearchTermInsightsInsightsInner.md) |  | [optional] 

## Example

```python
from openapi_client.models.search_term_insights import SearchTermInsights

# TODO update the JSON string below
json = "{}"
# create an instance of SearchTermInsights from a JSON string
search_term_insights_instance = SearchTermInsights.from_json(json)
# print the JSON string representation of the object
print(SearchTermInsights.to_json())

# convert the object into a dict
search_term_insights_dict = search_term_insights_instance.to_dict()
# create an instance of SearchTermInsights from a dict
search_term_insights_from_dict = SearchTermInsights.from_dict(search_term_insights_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


