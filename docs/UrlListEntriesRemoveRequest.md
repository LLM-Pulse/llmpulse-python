# UrlListEntriesRemoveRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**entry_ids** | **List[int]** |  | [optional] 
**values** | **List[str]** |  | [optional] 

## Example

```python
from llmpulse.models.url_list_entries_remove_request import UrlListEntriesRemoveRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListEntriesRemoveRequest from a JSON string
url_list_entries_remove_request_instance = UrlListEntriesRemoveRequest.from_json(json)
# print the JSON string representation of the object
print(UrlListEntriesRemoveRequest.to_json())

# convert the object into a dict
url_list_entries_remove_request_dict = url_list_entries_remove_request_instance.to_dict()
# create an instance of UrlListEntriesRemoveRequest from a dict
url_list_entries_remove_request_from_dict = UrlListEntriesRemoveRequest.from_dict(url_list_entries_remove_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


