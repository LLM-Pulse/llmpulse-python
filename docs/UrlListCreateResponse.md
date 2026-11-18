# UrlListCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url_list** | [**UrlListWithCounts**](UrlListWithCounts.md) |  | 
**entries_added** | **int** |  | 
**invalid_entries** | [**List[UrlListInvalidEntry]**](UrlListInvalidEntry.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.url_list_create_response import UrlListCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListCreateResponse from a JSON string
url_list_create_response_instance = UrlListCreateResponse.from_json(json)
# print the JSON string representation of the object
print(UrlListCreateResponse.to_json())

# convert the object into a dict
url_list_create_response_dict = url_list_create_response_instance.to_dict()
# create an instance of UrlListCreateResponse from a dict
url_list_create_response_from_dict = UrlListCreateResponse.from_dict(url_list_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


