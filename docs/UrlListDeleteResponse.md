# UrlListDeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**deleted** | **bool** |  | 
**id** | **int** |  | 
**name** | **str** |  | 
**entries_removed** | **int** |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.url_list_delete_response import UrlListDeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListDeleteResponse from a JSON string
url_list_delete_response_instance = UrlListDeleteResponse.from_json(json)
# print the JSON string representation of the object
print(UrlListDeleteResponse.to_json())

# convert the object into a dict
url_list_delete_response_dict = url_list_delete_response_instance.to_dict()
# create an instance of UrlListDeleteResponse from a dict
url_list_delete_response_from_dict = UrlListDeleteResponse.from_dict(url_list_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


