# PromptExecutionRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**prompt_id** | **int** |  | 
**executed_at** | **datetime** | Null while the answer is still pending | 
**duration_ms** | **float** |  | 
**success** | **bool** | Null while the answer is still pending | 
**model** | **str** |  | 
**fan_out_queries** | **List[str]** | Sub-queries the model issued while answering; null when the model reports none | 
**has_mention** | **bool** |  | 
**has_citation** | **bool** |  | 
**mentions_count** | **int** | 1 when the answer mentions the brand, otherwise 0 | 
**citations_count** | **int** | 1 when the answer cites the brand, otherwise 0 | 
**app_url** | **str** | Opens this answer in the app. The link names its project, so it opens there for any user with access to that project | 

## Example

```python
from llmpulse.models.prompt_execution_record import PromptExecutionRecord

# TODO update the JSON string below
json = "{}"
# create an instance of PromptExecutionRecord from a JSON string
prompt_execution_record_instance = PromptExecutionRecord.from_json(json)
# print the JSON string representation of the object
print(PromptExecutionRecord.to_json())

# convert the object into a dict
prompt_execution_record_dict = prompt_execution_record_instance.to_dict()
# create an instance of PromptExecutionRecord from a dict
prompt_execution_record_from_dict = PromptExecutionRecord.from_dict(prompt_execution_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


