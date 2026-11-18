# AiModelDeclinedAnswersResponse

How often one AI model declined to answer the project's prompts. An answer is a finished run of the model, a declined one included; a declined answer counts as no answer and never enters the metrics. The window starts at the tracking period holding its first day, and summary, chart and by_prompt count that same window.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**var_from** | **datetime** | Start of the tracking period holding the first day asked for | 
**to** | **datetime** |  | 
**model** | **str** | The model the counts are for | 
**cadence** | **str** | The account&#39;s current tracking cadence: daily, weekly or monthly. Chart periods before a switch from weekly to daily stay weekly. | 
**filters** | [**AiModelDeclinedAnswersResponseFilters**](AiModelDeclinedAnswersResponseFilters.md) |  | [optional] 
**summary** | [**AiModelDeclinedAnswersResponseSummary**](AiModelDeclinedAnswersResponseSummary.md) |  | 
**chart** | [**List[AiModelDeclinedAnswersResponseChartInner]**](AiModelDeclinedAnswersResponseChartInner.md) | One point per tracking period holding an answer, oldest first. A period without answers has no point; a period with answers and no declines is a real 0. | 
**by_prompt** | [**AiModelDeclinedAnswersResponseByPrompt**](AiModelDeclinedAnswersResponseByPrompt.md) |  | 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_declined_answers_response import AiModelDeclinedAnswersResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelDeclinedAnswersResponse from a JSON string
ai_model_declined_answers_response_instance = AiModelDeclinedAnswersResponse.from_json(json)
# print the JSON string representation of the object
print(AiModelDeclinedAnswersResponse.to_json())

# convert the object into a dict
ai_model_declined_answers_response_dict = ai_model_declined_answers_response_instance.to_dict()
# create an instance of AiModelDeclinedAnswersResponse from a dict
ai_model_declined_answers_response_from_dict = AiModelDeclinedAnswersResponse.from_dict(ai_model_declined_answers_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


