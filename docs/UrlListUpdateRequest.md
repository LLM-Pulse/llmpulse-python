# UrlListUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**currency** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.url_list_update_request import UrlListUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListUpdateRequest from a JSON string
url_list_update_request_instance = UrlListUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(UrlListUpdateRequest.to_json())

# convert the object into a dict
url_list_update_request_dict = url_list_update_request_instance.to_dict()
# create an instance of UrlListUpdateRequest from a dict
url_list_update_request_from_dict = UrlListUpdateRequest.from_dict(url_list_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


