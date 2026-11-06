# TargetingTargetingKeywordsIncluded


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phrase** | [**List[TargetingTargetingKeywordsIncludedPhraseInner]**](TargetingTargetingKeywordsIncludedPhraseInner.md) |  | [optional] 
**exact** | [**List[TargetingTargetingKeywordsIncludedExactInner]**](TargetingTargetingKeywordsIncludedExactInner.md) |  | [optional] 

## Example

```python
from openapi_client.models.targeting_targeting_keywords_included import TargetingTargetingKeywordsIncluded

# TODO update the JSON string below
json = "{}"
# create an instance of TargetingTargetingKeywordsIncluded from a JSON string
targeting_targeting_keywords_included_instance = TargetingTargetingKeywordsIncluded.from_json(json)
# print the JSON string representation of the object
print(TargetingTargetingKeywordsIncluded.to_json())

# convert the object into a dict
targeting_targeting_keywords_included_dict = targeting_targeting_keywords_included_instance.to_dict()
# create an instance of TargetingTargetingKeywordsIncluded from a dict
targeting_targeting_keywords_included_from_dict = TargetingTargetingKeywordsIncluded.from_dict(targeting_targeting_keywords_included_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


