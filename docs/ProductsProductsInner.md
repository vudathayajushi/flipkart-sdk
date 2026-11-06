# ProductsProductsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**image** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**min_price** | **float** |  | [optional] 
**max_price** | **float** |  | [optional] 
**currency** | **float** |  | [optional] 
**store_list** | **List[str]** |  | [optional] 
**brand** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.products_products_inner import ProductsProductsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ProductsProductsInner from a JSON string
products_products_inner_instance = ProductsProductsInner.from_json(json)
# print the JSON string representation of the object
print(ProductsProductsInner.to_json())

# convert the object into a dict
products_products_inner_dict = products_products_inner_instance.to_dict()
# create an instance of ProductsProductsInner from a dict
products_products_inner_from_dict = ProductsProductsInner.from_dict(products_products_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


