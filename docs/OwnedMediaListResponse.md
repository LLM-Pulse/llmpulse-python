# OwnedMediaListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**provider** | **str** |  | [optional] 
**view** | **str** |  | [optional] 
**store** | **str** | provider&#x3D;mobile_apps only | [optional] 
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[OwnedMediaRow]**](OwnedMediaRow.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_list_response import OwnedMediaListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaListResponse from a JSON string
owned_media_list_response_instance = OwnedMediaListResponse.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaListResponse.to_json())

# convert the object into a dict
owned_media_list_response_dict = owned_media_list_response_instance.to_dict()
# create an instance of OwnedMediaListResponse from a dict
owned_media_list_response_from_dict = OwnedMediaListResponse.from_dict(owned_media_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


