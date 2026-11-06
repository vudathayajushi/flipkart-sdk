# CampaignRules


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rules** | **List[str]** | List of rule IDs associated with the campaign | [optional] 

## Example

```python
from openapi_client.models.campaign_rules import CampaignRules

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignRules from a JSON string
campaign_rules_instance = CampaignRules.from_json(json)
# print the JSON string representation of the object
print(CampaignRules.to_json())

# convert the object into a dict
campaign_rules_dict = campaign_rules_instance.to_dict()
# create an instance of CampaignRules from a dict
campaign_rules_from_dict = CampaignRules.from_dict(campaign_rules_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


