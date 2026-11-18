# UrlListsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**filters** | [**UrlListFilters**](UrlListFilters.md) |  | 
**total** | **int** |  | 
**data** | [**List[UrlListWithStats]**](UrlListWithStats.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.url_lists_response import UrlListsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListsResponse from a JSON string
url_lists_response_instance = UrlListsResponse.from_json(json)
# print the JSON string representation of the object
print(UrlListsResponse.to_json())

# convert the object into a dict
url_lists_response_dict = url_lists_response_instance.to_dict()
# create an instance of UrlListsResponse from a dict
url_lists_response_from_dict = UrlListsResponse.from_dict(url_lists_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


