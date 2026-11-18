# UrlListEntriesRemoveResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url_list_id** | **int** |  | 
**removed** | **int** |  | 
**entries_count** | **int** |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.url_list_entries_remove_response import UrlListEntriesRemoveResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListEntriesRemoveResponse from a JSON string
url_list_entries_remove_response_instance = UrlListEntriesRemoveResponse.from_json(json)
# print the JSON string representation of the object
print(UrlListEntriesRemoveResponse.to_json())

# convert the object into a dict
url_list_entries_remove_response_dict = url_list_entries_remove_response_instance.to_dict()
# create an instance of UrlListEntriesRemoveResponse from a dict
url_list_entries_remove_response_from_dict = UrlListEntriesRemoveResponse.from_dict(url_list_entries_remove_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


