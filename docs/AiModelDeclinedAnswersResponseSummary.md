# AiModelDeclinedAnswersResponseSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**answers** | **int** | Finished runs of the model, declined ones included | [optional] 
**declined** | **int** | Answers the model declined | [optional] 
**decline_rate** | **float** |  | [optional] 
**safety_filter** | **int** | Answers declined by the model&#39;s own safety filters | [optional] 
**safety_filter_rate** | **float** |  | [optional] 
**topic_refusal** | **int** | Answers that declined the topic itself, such as tobacco, gambling or alcohol | [optional] 
**topic_refusal_rate** | **float** |  | [optional] 
**last_declined_at** | **datetime** | When the latest declined answer of the window was created; null when none was declined | [optional] 

## Example

```python
from llmpulse.models.ai_model_declined_answers_response_summary import AiModelDeclinedAnswersResponseSummary

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelDeclinedAnswersResponseSummary from a JSON string
ai_model_declined_answers_response_summary_instance = AiModelDeclinedAnswersResponseSummary.from_json(json)
# print the JSON string representation of the object
print(AiModelDeclinedAnswersResponseSummary.to_json())

# convert the object into a dict
ai_model_declined_answers_response_summary_dict = ai_model_declined_answers_response_summary_instance.to_dict()
# create an instance of AiModelDeclinedAnswersResponseSummary from a dict
ai_model_declined_answers_response_summary_from_dict = AiModelDeclinedAnswersResponseSummary.from_dict(ai_model_declined_answers_response_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


