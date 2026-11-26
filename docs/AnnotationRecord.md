# AnnotationRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**title** | **str** |  | 
**description** | **str** |  | 
**annotation_date** | **date** |  | 
**color** | **str** |  | 
**category** | **str** | user (written by a person) or system (added by the platform) | 
**origin** | **str** | manual, platform (a platform-wide event) or automation (a project change recorded automatically) | 
**annotation_category** | [**AnnotationRecordAnnotationCategory**](AnnotationRecordAnnotationCategory.md) |  | 
**editable** | **bool** | Whether the requesting user may update or delete it | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.annotation_record import AnnotationRecord

# TODO update the JSON string below
json = "{}"
# create an instance of AnnotationRecord from a JSON string
annotation_record_instance = AnnotationRecord.from_json(json)
# print the JSON string representation of the object
print(AnnotationRecord.to_json())

# convert the object into a dict
annotation_record_dict = annotation_record_instance.to_dict()
# create an instance of AnnotationRecord from a dict
annotation_record_from_dict = AnnotationRecord.from_dict(annotation_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


