# AiModelDeclineCounts

Answers and declined answers, by reason. A rate is a percentage of the answers, null with no answer behind it.

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

## Example

```python
from llmpulse.models.ai_model_decline_counts import AiModelDeclineCounts

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelDeclineCounts from a JSON string
ai_model_decline_counts_instance = AiModelDeclineCounts.from_json(json)
# print the JSON string representation of the object
print(AiModelDeclineCounts.to_json())

# convert the object into a dict
ai_model_decline_counts_dict = ai_model_decline_counts_instance.to_dict()
# create an instance of AiModelDeclineCounts from a dict
ai_model_decline_counts_from_dict = AiModelDeclineCounts.from_dict(ai_model_decline_counts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


