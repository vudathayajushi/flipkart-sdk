# Campaign


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique identifier for the campaign | [optional] 
**name** | **str** | Name of the campaign | [optional] 
**status** | **str** | Current status of the campaign | [optional] 
**budget_type** | **str** | Budget Type of campaign | [optional] 
**type** | **str** | Type of campaign | [optional] 
**start_date** | **float** |  | [optional] 
**end_date** | **float** |  | [optional] 
**budget** | **float** |  | [optional] 
**cost_model** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.campaign import Campaign

# TODO update the JSON string below
json = "{}"
# create an instance of Campaign from a JSON string
campaign_instance = Campaign.from_json(json)
# print the JSON string representation of the object
print(Campaign.to_json())

# convert the object into a dict
campaign_dict = campaign_instance.to_dict()
# create an instance of Campaign from a dict
campaign_from_dict = Campaign.from_dict(campaign_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


