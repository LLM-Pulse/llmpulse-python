# AiOverviewResultsResponseByPrompt

One row per prompt with an AI Overview run in the window, highest result rate first, then more runs and the prompt id

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Prompts with an AI Overview run in the window | 
**data** | [**List[AiOverviewResultsResponseByPromptDataInner]**](AiOverviewResultsResponseByPromptDataInner.md) |  | 

## Example

```python
from llmpulse.models.ai_overview_results_response_by_prompt import AiOverviewResultsResponseByPrompt

# TODO update the JSON string below
json = "{}"
# create an instance of AiOverviewResultsResponseByPrompt from a JSON string
ai_overview_results_response_by_prompt_instance = AiOverviewResultsResponseByPrompt.from_json(json)
# print the JSON string representation of the object
print(AiOverviewResultsResponseByPrompt.to_json())

# convert the object into a dict
ai_overview_results_response_by_prompt_dict = ai_overview_results_response_by_prompt_instance.to_dict()
# create an instance of AiOverviewResultsResponseByPrompt from a dict
ai_overview_results_response_by_prompt_from_dict = AiOverviewResultsResponseByPrompt.from_dict(ai_overview_results_response_by_prompt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


