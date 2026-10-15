# PromptGenerationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **UUID** | The run id; poll GET /prompt_generations/{id} with it (kept for 24 hours) | 
**project_id** | **int** |  | 
**source** | **str** |  | 
**status** | **str** |  | 
**params** | [**PromptGenerationResponseParams**](PromptGenerationResponseParams.md) |  | 
**created_at** | **datetime** |  | 
**finished_at** | **datetime** |  | 
**suggestions_count** | **int** |  | 
**suggestions** | [**List[SuggestedPrompt]**](SuggestedPrompt.md) | The suggestions the run saved to the Suggested prompts queue, with their current status | 
**error** | [**PromptGenerationResponseError**](PromptGenerationResponseError.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.prompt_generation_response import PromptGenerationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptGenerationResponse from a JSON string
prompt_generation_response_instance = PromptGenerationResponse.from_json(json)
# print the JSON string representation of the object
print(PromptGenerationResponse.to_json())

# convert the object into a dict
prompt_generation_response_dict = prompt_generation_response_instance.to_dict()
# create an instance of PromptGenerationResponse from a dict
prompt_generation_response_from_dict = PromptGenerationResponse.from_dict(prompt_generation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


