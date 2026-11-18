# AiModelDeclinedAnswersResponseByPrompt

One row per prompt with an answer in the window, highest decline rate first, then more declines, more answers and the prompt id

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** | Prompts with an answer in the window | [optional] 
**data** | [**List[AiModelDeclinedAnswersResponseByPromptDataInner]**](AiModelDeclinedAnswersResponseByPromptDataInner.md) |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_declined_answers_response_by_prompt import AiModelDeclinedAnswersResponseByPrompt

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelDeclinedAnswersResponseByPrompt from a JSON string
ai_model_declined_answers_response_by_prompt_instance = AiModelDeclinedAnswersResponseByPrompt.from_json(json)
# print the JSON string representation of the object
print(AiModelDeclinedAnswersResponseByPrompt.to_json())

# convert the object into a dict
ai_model_declined_answers_response_by_prompt_dict = ai_model_declined_answers_response_by_prompt_instance.to_dict()
# create an instance of AiModelDeclinedAnswersResponseByPrompt from a dict
ai_model_declined_answers_response_by_prompt_from_dict = AiModelDeclinedAnswersResponseByPrompt.from_dict(ai_model_declined_answers_response_by_prompt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


