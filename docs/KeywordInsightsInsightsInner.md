# KeywordInsightsInsightsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metrics** | [**MetricsMetrics**](MetricsMetrics.md) |  | [optional] 
**attributed_keyword** | **str** |  | [optional] 
**keyword_match_type** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.keyword_insights_insights_inner import KeywordInsightsInsightsInner

# TODO update the JSON string below
json = "{}"
# create an instance of KeywordInsightsInsightsInner from a JSON string
keyword_insights_insights_inner_instance = KeywordInsightsInsightsInner.from_json(json)
# print the JSON string representation of the object
print(KeywordInsightsInsightsInner.to_json())

# convert the object into a dict
keyword_insights_insights_inner_dict = keyword_insights_insights_inner_instance.to_dict()
# create an instance of KeywordInsightsInsightsInner from a dict
keyword_insights_insights_inner_from_dict = KeywordInsightsInsightsInner.from_dict(keyword_insights_insights_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


