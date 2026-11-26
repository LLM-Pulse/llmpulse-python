# AnnotationDeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**deleted** | **bool** | Always true | 
**id** | **int** |  | 
**title** | **str** |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.annotation_delete_response import AnnotationDeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AnnotationDeleteResponse from a JSON string
annotation_delete_response_instance = AnnotationDeleteResponse.from_json(json)
# print the JSON string representation of the object
print(AnnotationDeleteResponse.to_json())

# convert the object into a dict
annotation_delete_response_dict = annotation_delete_response_instance.to_dict()
# create an instance of AnnotationDeleteResponse from a dict
annotation_delete_response_from_dict = AnnotationDeleteResponse.from_dict(annotation_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


