# UrlListUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url_list** | [**UrlListWithCounts**](UrlListWithCounts.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.url_list_update_response import UrlListUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UrlListUpdateResponse from a JSON string
url_list_update_response_instance = UrlListUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(UrlListUpdateResponse.to_json())

# convert the object into a dict
url_list_update_response_dict = url_list_update_response_instance.to_dict()
# create an instance of UrlListUpdateResponse from a dict
url_list_update_response_from_dict = UrlListUpdateResponse.from_dict(url_list_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


