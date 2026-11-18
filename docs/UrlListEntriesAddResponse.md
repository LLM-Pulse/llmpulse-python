# UrlListEntriesAddResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url_list_id** | **int** |  | 
**added** | **int** |  | 
**updated** | **int** |  | 
**invalid_entries** | [**List[UrlListInvalidEntry]**](UrlListInvalidEntry.md) |  | 
**entries_count** | **int** |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.url_list_entries_add_response import UrlListEntriesAddResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListEntriesAddResponse from a JSON string
url_list_entries_add_response_instance = UrlListEntriesAddResponse.from_json(json)
# print the JSON string representation of the object
print(UrlListEntriesAddResponse.to_json())

# convert the object into a dict
url_list_entries_add_response_dict = url_list_entries_add_response_instance.to_dict()
# create an instance of UrlListEntriesAddResponse from a dict
url_list_entries_add_response_from_dict = UrlListEntriesAddResponse.from_dict(url_list_entries_add_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


