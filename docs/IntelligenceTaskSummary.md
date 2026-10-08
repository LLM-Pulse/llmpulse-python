# IntelligenceTaskSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**public_id** | **str** |  | 
**task_type** | **str** |  | 
**title** | **str** |  | 
**status** | **str** |  | 
**prompt_id** | **int** |  | 
**prompt_text** | **str** |  | 
**word_count** | **int** |  | 
**manually_edited_at** | **datetime** | When the content was last edited by hand; null while the output is as generated | 
**created_at** | **datetime** |  | 
**processed_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.intelligence_task_summary import IntelligenceTaskSummary

# TODO update the JSON string below
json = "{}"
# create an instance of IntelligenceTaskSummary from a JSON string
intelligence_task_summary_instance = IntelligenceTaskSummary.from_json(json)
# print the JSON string representation of the object
print(IntelligenceTaskSummary.to_json())

# convert the object into a dict
intelligence_task_summary_dict = intelligence_task_summary_instance.to_dict()
# create an instance of IntelligenceTaskSummary from a dict
intelligence_task_summary_from_dict = IntelligenceTaskSummary.from_dict(intelligence_task_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


