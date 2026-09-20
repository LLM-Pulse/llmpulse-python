# IntelligenceTaskUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**edits** | **Dict[str, str]** | Dotted result_data paths (title, sections.0.content, key_points.2) mapped to their replacement text. Only string fields that already exist are editable; sections cannot be added or removed. | 

## Example

```python
from llmpulse.models.intelligence_task_update_request import IntelligenceTaskUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IntelligenceTaskUpdateRequest from a JSON string
intelligence_task_update_request_instance = IntelligenceTaskUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(IntelligenceTaskUpdateRequest.to_json())

# convert the object into a dict
intelligence_task_update_request_dict = intelligence_task_update_request_instance.to_dict()
# create an instance of IntelligenceTaskUpdateRequest from a dict
intelligence_task_update_request_from_dict = IntelligenceTaskUpdateRequest.from_dict(intelligence_task_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


