# BulkCampaigns


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[BulkCampaignsDataInner]**](BulkCampaignsDataInner.md) |  | [optional] 

## Example

```python
from openapi_client.models.bulk_campaigns import BulkCampaigns

# TODO update the JSON string below
json = "{}"
# create an instance of BulkCampaigns from a JSON string
bulk_campaigns_instance = BulkCampaigns.from_json(json)
# print the JSON string representation of the object
print(BulkCampaigns.to_json())

# convert the object into a dict
bulk_campaigns_dict = bulk_campaigns_instance.to_dict()
# create an instance of BulkCampaigns from a dict
bulk_campaigns_from_dict = BulkCampaigns.from_dict(bulk_campaigns_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


