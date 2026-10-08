# AnnotationCreateResponseAnnotation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**title** | **str** |  | 
**annotation_date** | **date** |  | 
**description** | **str** |  | 
**color** | **str** | Hex color such as &#39;#4F46E5&#39; | 
**annotation_category_id** | **int** |  | 

## Example

```python
from llmpulse.models.annotation_create_response_annotation import AnnotationCreateResponseAnnotation

# TODO update the JSON string below
json = "{}"
# create an instance of AnnotationCreateResponseAnnotation from a JSON string
annotation_create_response_annotation_instance = AnnotationCreateResponseAnnotation.from_json(json)
# print the JSON string representation of the object
print(AnnotationCreateResponseAnnotation.to_json())

# convert the object into a dict
annotation_create_response_annotation_dict = annotation_create_response_annotation_instance.to_dict()
# create an instance of AnnotationCreateResponseAnnotation from a dict
annotation_create_response_annotation_from_dict = AnnotationCreateResponseAnnotation.from_dict(annotation_create_response_annotation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


