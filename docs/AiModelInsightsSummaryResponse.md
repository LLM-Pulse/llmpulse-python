# AiModelInsightsSummaryResponse

One entry per AI model the account has enabled or that answered in the window, in the in-app column order: the models list, which every per-model list and map in summary follows. A share, net sentiment or market share value with nothing behind it is null, because 0 is a real value; counts, totals and weighted visibility scores stay 0.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**filters** | [**AiModelInsightsFiltersEcho**](AiModelInsightsFiltersEcho.md) |  | [optional] 
**models** | [**List[AiModelInsightsModel]**](AiModelInsightsModel.md) | The AI models the account has enabled or that answered in the window, in the in-app column order | [optional] 
**summary** | [**AiModelInsightsSummaryResponseSummary**](AiModelInsightsSummaryResponseSummary.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_summary_response import AiModelInsightsSummaryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsSummaryResponse from a JSON string
ai_model_insights_summary_response_instance = AiModelInsightsSummaryResponse.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsSummaryResponse.to_json())

# convert the object into a dict
ai_model_insights_summary_response_dict = ai_model_insights_summary_response_instance.to_dict()
# create an instance of AiModelInsightsSummaryResponse from a dict
ai_model_insights_summary_response_from_dict = AiModelInsightsSummaryResponse.from_dict(ai_model_insights_summary_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


