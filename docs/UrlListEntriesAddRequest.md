# UrlListEntriesAddRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**entries** | [**List[UrlListEntryInput]**](UrlListEntryInput.md) |  | 
**match_type** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.url_list_entries_add_request import UrlListEntriesAddRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListEntriesAddRequest from a JSON string
url_list_entries_add_request_instance = UrlListEntriesAddRequest.from_json(json)
# print the JSON string representation of the object
print(UrlListEntriesAddRequest.to_json())

# convert the object into a dict
url_list_entries_add_request_dict = url_list_entries_add_request_instance.to_dict()
# create an instance of UrlListEntriesAddRequest from a dict
url_list_entries_add_request_from_dict = UrlListEntriesAddRequest.from_dict(url_list_entries_add_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


