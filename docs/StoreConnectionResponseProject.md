# StoreConnectionResponseProject

The live project the store maps to: its domain equals the store's, or is a parent or subdomain of it. Null when no project matches

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**domain** | **str** |  | 
**country_code** | **str** |  | [optional] 
**language_code** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.store_connection_response_project import StoreConnectionResponseProject

# TODO update the JSON string below
json = "{}"
# create an instance of StoreConnectionResponseProject from a JSON string
store_connection_response_project_instance = StoreConnectionResponseProject.from_json(json)
# print the JSON string representation of the object
print(StoreConnectionResponseProject.to_json())

# convert the object into a dict
store_connection_response_project_dict = store_connection_response_project_instance.to_dict()
# create an instance of StoreConnectionResponseProject from a dict
store_connection_response_project_from_dict = StoreConnectionResponseProject.from_dict(store_connection_response_project_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


