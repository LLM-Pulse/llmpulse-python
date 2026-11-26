# AnnotationsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[AnnotationRecord]**](AnnotationRecord.md) |  | 

## Example

```python
from llmpulse.models.annotations_response import AnnotationsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AnnotationsResponse from a JSON string
annotations_response_instance = AnnotationsResponse.from_json(json)
# print the JSON string representation of the object
print(AnnotationsResponse.to_json())

# convert the object into a dict
annotations_response_dict = annotations_response_instance.to_dict()
# create an instance of AnnotationsResponse from a dict
annotations_response_from_dict = AnnotationsResponse.from_dict(annotations_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


