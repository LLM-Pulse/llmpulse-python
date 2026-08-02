# UpdateAnnotationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**title** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**annotation_date** | **date** |  | [optional] 
**color** | **str** |  | [optional] 
**annotation_category_id** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.update_annotation_request import UpdateAnnotationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateAnnotationRequest from a JSON string
update_annotation_request_instance = UpdateAnnotationRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateAnnotationRequest.to_json())

# convert the object into a dict
update_annotation_request_dict = update_annotation_request_instance.to_dict()
# create an instance of UpdateAnnotationRequest from a dict
update_annotation_request_from_dict = UpdateAnnotationRequest.from_dict(update_annotation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


