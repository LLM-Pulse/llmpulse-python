# UrlListCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**currency** | **str** |  | [optional] [default to 'USD']
**entries** | [**List[UrlListEntryInput]**](UrlListEntryInput.md) |  | [optional] 
**match_type** | **str** | Read every entry without its own match_type as this type. Default detects it from each value. | [optional] 

## Example

```python
from llmpulse.models.url_list_create_request import UrlListCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListCreateRequest from a JSON string
url_list_create_request_instance = UrlListCreateRequest.from_json(json)
# print the JSON string representation of the object
print(UrlListCreateRequest.to_json())

# convert the object into a dict
url_list_create_request_dict = url_list_create_request_instance.to_dict()
# create an instance of UrlListCreateRequest from a dict
url_list_create_request_from_dict = UrlListCreateRequest.from_dict(url_list_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


