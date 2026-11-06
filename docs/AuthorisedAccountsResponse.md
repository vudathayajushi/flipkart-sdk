# AuthorisedAccountsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**next_cursor** | **str** | Cursor for pagination. Empty when there are no more pages. | [optional] 
**data** | [**Dict[str, AuthorisedAccount]**](AuthorisedAccount.md) | Map of account ID to account details | [optional] 

## Example

```python
from openapi_client.models.authorised_accounts_response import AuthorisedAccountsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AuthorisedAccountsResponse from a JSON string
authorised_accounts_response_instance = AuthorisedAccountsResponse.from_json(json)
# print the JSON string representation of the object
print(AuthorisedAccountsResponse.to_json())

# convert the object into a dict
authorised_accounts_response_dict = authorised_accounts_response_instance.to_dict()
# create an instance of AuthorisedAccountsResponse from a dict
authorised_accounts_response_from_dict = AuthorisedAccountsResponse.from_dict(authorised_accounts_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


