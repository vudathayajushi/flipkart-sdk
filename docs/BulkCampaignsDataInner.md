# BulkCampaignsDataInner


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
**pacing** | **str** | &#x60;pacing &#x3D; NONE&#x60; refers to when \&quot;Equally Divide Budget for All Days\&quot; checkbox is Unchecked (this is the default set for campaigns) &lt;br&gt; &#x60;pacing &#x3D; EVEN&#x60; refers to when \&quot;Equally Divide Budget for All Days\&quot; checkbox is Checked &lt;br&gt; (This option is available only if end date time is specified and the &#x60;\&quot;budgetType\&quot; &#x3D;  \&quot;TOTAL_BUDGET\&quot;&#x60;) | [optional] 
**ad_groups** | [**List[AdGroupBulk]**](AdGroupBulk.md) |  | [optional] 

## Example

```python
from openapi_client.models.bulk_campaigns_data_inner import BulkCampaignsDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of BulkCampaignsDataInner from a JSON string
bulk_campaigns_data_inner_instance = BulkCampaignsDataInner.from_json(json)
# print the JSON string representation of the object
print(BulkCampaignsDataInner.to_json())

# convert the object into a dict
bulk_campaigns_data_inner_dict = bulk_campaigns_data_inner_instance.to_dict()
# create an instance of BulkCampaignsDataInner from a dict
bulk_campaigns_data_inner_from_dict = BulkCampaignsDataInner.from_dict(bulk_campaigns_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


