# KeywordInsights

Insights for keyword at adgroup level for account

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**insights** | [**List[KeywordInsightsInsightsInner]**](KeywordInsightsInsightsInner.md) |  | [optional] 

## Example

```python
from openapi_client.models.keyword_insights import KeywordInsights

# TODO update the JSON string below
json = "{}"
# create an instance of KeywordInsights from a JSON string
keyword_insights_instance = KeywordInsights.from_json(json)
# print the JSON string representation of the object
print(KeywordInsights.to_json())

# convert the object into a dict
keyword_insights_dict = keyword_insights_instance.to_dict()
# create an instance of KeywordInsights from a dict
keyword_insights_from_dict = KeywordInsights.from_dict(keyword_insights_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


