# MetricsMetrics


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cost** | **float** |  | [optional] 
**view** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** |  | [optional] 
**cvr** | **float** |  | [optional] 
**cpc** | **float** |  | [optional] 
**roi** | **float** |  | [optional] 
**indirect_units** | **int** |  | [optional] 
**direct_units** | **int** |  | [optional] 
**direct_revenue** | **float** |  | [optional] 
**indirect_revenue** | **float** |  | [optional] 
**ctr_percent** | **float** |  | [optional] 
**direct_cvr_percent** | **float** |  | [optional] 
**indirect_cvr_percent** | **float** |  | [optional] 

## Example

```python
from openapi_client.models.metrics_metrics import MetricsMetrics

# TODO update the JSON string below
json = "{}"
# create an instance of MetricsMetrics from a JSON string
metrics_metrics_instance = MetricsMetrics.from_json(json)
# print the JSON string representation of the object
print(MetricsMetrics.to_json())

# convert the object into a dict
metrics_metrics_dict = metrics_metrics_instance.to_dict()
# create an instance of MetricsMetrics from a dict
metrics_metrics_from_dict = MetricsMetrics.from_dict(metrics_metrics_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


