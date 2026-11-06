# TargetingTargetingKeywords


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**excluded** | [**List[TargetingTargetingKeywordsExcludedInner]**](TargetingTargetingKeywordsExcludedInner.md) |  | [optional] 
**included** | [**TargetingTargetingKeywordsIncluded**](TargetingTargetingKeywordsIncluded.md) |  | [optional] 

## Example

```python
from openapi_client.models.targeting_targeting_keywords import TargetingTargetingKeywords

# TODO update the JSON string below
json = "{}"
# create an instance of TargetingTargetingKeywords from a JSON string
targeting_targeting_keywords_instance = TargetingTargetingKeywords.from_json(json)
# print the JSON string representation of the object
print(TargetingTargetingKeywords.to_json())

# convert the object into a dict
targeting_targeting_keywords_dict = targeting_targeting_keywords_instance.to_dict()
# create an instance of TargetingTargetingKeywords from a dict
targeting_targeting_keywords_from_dict = TargetingTargetingKeywords.from_dict(targeting_targeting_keywords_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


