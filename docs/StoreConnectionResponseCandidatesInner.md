# StoreConnectionResponseCandidatesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**domain** | **str** | Empty when the project has no website URL | 

## Example

```python
from llmpulse.models.store_connection_response_candidates_inner import StoreConnectionResponseCandidatesInner

# TODO update the JSON string below
json = "{}"
# create an instance of StoreConnectionResponseCandidatesInner from a JSON string
store_connection_response_candidates_inner_instance = StoreConnectionResponseCandidatesInner.from_json(json)
# print the JSON string representation of the object
print(StoreConnectionResponseCandidatesInner.to_json())

# convert the object into a dict
store_connection_response_candidates_inner_dict = store_connection_response_candidates_inner_instance.to_dict()
# create an instance of StoreConnectionResponseCandidatesInner from a dict
store_connection_response_candidates_inner_from_dict = StoreConnectionResponseCandidatesInner.from_dict(store_connection_response_candidates_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


