# AuthorisedAccount


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique identifier for the account | [optional] 
**name** | **str** | Display name of the account | [optional] 
**parent_id** | **str** | Parent business account ID. Empty for seller accounts. | [optional] 
**status** | **str** | Account status | [optional] 
**type** | **str** | Account type | [optional] 
**account_type** | **str** | Account classification | [optional] 
**access_level** | **str** | Permission level granted to the token holder | [optional] 

## Example

```python
from openapi_client.models.authorised_account import AuthorisedAccount

# TODO update the JSON string below
json = "{}"
# create an instance of AuthorisedAccount from a JSON string
authorised_account_instance = AuthorisedAccount.from_json(json)
# print the JSON string representation of the object
print(AuthorisedAccount.to_json())

# convert the object into a dict
authorised_account_dict = authorised_account_instance.to_dict()
# create an instance of AuthorisedAccount from a dict
authorised_account_from_dict = AuthorisedAccount.from_dict(authorised_account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


