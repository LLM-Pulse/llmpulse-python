# AnnotationUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**annotation** | [**AnnotationRecord**](AnnotationRecord.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.annotation_update_response import AnnotationUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AnnotationUpdateResponse from a JSON string
annotation_update_response_instance = AnnotationUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(AnnotationUpdateResponse.to_json())

# convert the object into a dict
annotation_update_response_dict = annotation_update_response_instance.to_dict()
# create an instance of AnnotationUpdateResponse from a dict
annotation_update_response_from_dict = AnnotationUpdateResponse.from_dict(annotation_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


