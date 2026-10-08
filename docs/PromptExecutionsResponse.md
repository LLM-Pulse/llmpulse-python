# PromptExecutionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[PromptExecutionRecord]**](PromptExecutionRecord.md) |  | 

## Example

```python
from llmpulse.models.prompt_executions_response import PromptExecutionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptExecutionsResponse from a JSON string
prompt_executions_response_instance = PromptExecutionsResponse.from_json(json)
# print the JSON string representation of the object
print(PromptExecutionsResponse.to_json())

# convert the object into a dict
prompt_executions_response_dict = prompt_executions_response_instance.to_dict()
# create an instance of PromptExecutionsResponse from a dict
prompt_executions_response_from_dict = PromptExecutionsResponse.from_dict(prompt_executions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


