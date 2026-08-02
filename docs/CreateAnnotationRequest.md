# CreateAnnotationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**title** | **str** |  | 
**annotation_date** | **date** | ISO YYYY-MM-DD; defaults to today | [optional] 
**description** | **str** |  | [optional] 
**color** | **str** | Hex color, e.g. #2563eb | [optional] 
**annotation_category_id** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.create_annotation_request import CreateAnnotationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAnnotationRequest from a JSON string
create_annotation_request_instance = CreateAnnotationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateAnnotationRequest.to_json())

# convert the object into a dict
create_annotation_request_dict = create_annotation_request_instance.to_dict()
# create an instance of CreateAnnotationRequest from a dict
create_annotation_request_from_dict = CreateAnnotationRequest.from_dict(create_annotation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


