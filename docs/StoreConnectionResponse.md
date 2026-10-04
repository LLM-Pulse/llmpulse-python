# StoreConnectionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **str** | The store platform, e.g. shopify | 
**domain** | **str** | The store domain as compared: lowercase, without scheme, www or path | 
**project** | [**StoreConnectionResponseProject**](StoreConnectionResponseProject.md) |  | 
**ambiguous** | **bool** | True when several live projects match the store domain (for example one project per market). project is then null and the app asks the key holder to pick from candidates. | 
**candidates** | [**List[StoreConnectionResponseCandidatesInner]**](StoreConnectionResponseCandidatesInner.md) | Every live project of the account, for a project picker | 
**account** | [**StoreConnectionResponseAccount**](StoreConnectionResponseAccount.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.store_connection_response import StoreConnectionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of StoreConnectionResponse from a JSON string
store_connection_response_instance = StoreConnectionResponse.from_json(json)
# print the JSON string representation of the object
print(StoreConnectionResponse.to_json())

# convert the object into a dict
store_connection_response_dict = store_connection_response_instance.to_dict()
# create an instance of StoreConnectionResponse from a dict
store_connection_response_from_dict = StoreConnectionResponse.from_dict(store_connection_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


