# AiOverviewResultsResponseByPromptDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompt_id** | **int** |  | 
**prompt_text** | **str** |  | 
**total_responses** | **int** |  | 
**responses_with_results** | **int** |  | 
**result_rate** | **float** |  | 

## Example

```python
from llmpulse.models.ai_overview_results_response_by_prompt_data_inner import AiOverviewResultsResponseByPromptDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of AiOverviewResultsResponseByPromptDataInner from a JSON string
ai_overview_results_response_by_prompt_data_inner_instance = AiOverviewResultsResponseByPromptDataInner.from_json(json)
# print the JSON string representation of the object
print(AiOverviewResultsResponseByPromptDataInner.to_json())

# convert the object into a dict
ai_overview_results_response_by_prompt_data_inner_dict = ai_overview_results_response_by_prompt_data_inner_instance.to_dict()
# create an instance of AiOverviewResultsResponseByPromptDataInner from a dict
ai_overview_results_response_by_prompt_data_inner_from_dict = AiOverviewResultsResponseByPromptDataInner.from_dict(ai_overview_results_response_by_prompt_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


