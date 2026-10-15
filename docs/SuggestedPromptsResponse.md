# SuggestedPromptsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** |  | 
**data** | [**List[SuggestedPrompt]**](SuggestedPrompt.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.suggested_prompts_response import SuggestedPromptsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestedPromptsResponse from a JSON string
suggested_prompts_response_instance = SuggestedPromptsResponse.from_json(json)
# print the JSON string representation of the object
print(SuggestedPromptsResponse.to_json())

# convert the object into a dict
suggested_prompts_response_dict = suggested_prompts_response_instance.to_dict()
# create an instance of SuggestedPromptsResponse from a dict
suggested_prompts_response_from_dict = SuggestedPromptsResponse.from_dict(suggested_prompts_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


