# IntelligenceTask


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**public_id** | **str** |  | [optional] 
**project_id** | **int** |  | [optional] 
**task_type** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**prompt_id** | **int** |  | [optional] 
**prompt_text** | **str** |  | [optional] 
**agentic_mode** | **bool** |  | [optional] 
**custom_topic** | **str** |  | [optional] 
**user_instructions** | **str** |  | [optional] 
**output_language_code** | **str** |  | [optional] 
**word_count** | **int** |  | [optional] 
**result_data** | **object** | The generated content once status is completed; null before that | [optional] 
**error_message** | **str** |  | [optional] 
**estimated_time** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**processed_at** | **datetime** |  | [optional] 
**manually_edited_at** | **datetime** | When the content was last edited by hand; null while the output is as generated | [optional] 
**edited_by_user_id** | **int** | User behind the last manual edit; null for an unedited task or an edit made from an embedded portal | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.intelligence_task import IntelligenceTask

# TODO update the JSON string below
json = "{}"
# create an instance of IntelligenceTask from a JSON string
intelligence_task_instance = IntelligenceTask.from_json(json)
# print the JSON string representation of the object
print(IntelligenceTask.to_json())

# convert the object into a dict
intelligence_task_dict = intelligence_task_instance.to_dict()
# create an instance of IntelligenceTask from a dict
intelligence_task_from_dict = IntelligenceTask.from_dict(intelligence_task_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


