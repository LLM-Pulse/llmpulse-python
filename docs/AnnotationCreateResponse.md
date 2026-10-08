# AnnotationCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**annotation** | [**AnnotationCreateResponseAnnotation**](AnnotationCreateResponseAnnotation.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.annotation_create_response import AnnotationCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AnnotationCreateResponse from a JSON string
annotation_create_response_instance = AnnotationCreateResponse.from_json(json)
# print the JSON string representation of the object
print(AnnotationCreateResponse.to_json())

# convert the object into a dict
annotation_create_response_dict = annotation_create_response_instance.to_dict()
# create an instance of AnnotationCreateResponse from a dict
annotation_create_response_from_dict = AnnotationCreateResponse.from_dict(annotation_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


