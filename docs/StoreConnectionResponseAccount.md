# StoreConnectionResponseAccount


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan** | **str** | Internal plan key of the account, e.g. scale or scaleplus; null for a key limited to some projects | [optional] 

## Example

```python
from llmpulse.models.store_connection_response_account import StoreConnectionResponseAccount

# TODO update the JSON string below
json = "{}"
# create an instance of StoreConnectionResponseAccount from a JSON string
store_connection_response_account_instance = StoreConnectionResponseAccount.from_json(json)
# print the JSON string representation of the object
print(StoreConnectionResponseAccount.to_json())

# convert the object into a dict
store_connection_response_account_dict = store_connection_response_account_instance.to_dict()
# create an instance of StoreConnectionResponseAccount from a dict
store_connection_response_account_from_dict = StoreConnectionResponseAccount.from_dict(store_connection_response_account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


