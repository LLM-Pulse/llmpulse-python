# AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_weighted_visibility_score** | **float** | The brand&#39;s AI Visibility Score across the enabled models, its points there divided by the tracking runs with answers in any of them (the Overview&#39;s number for the same filters; a model that answered while disabled keeps its row but stays out of it); 0 when it has none | [optional] 
**models** | [**List[AiModelWeightedVisibilityRow]**](AiModelWeightedVisibilityRow.md) |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_summary_response_summary_weighted_visibility_by_model import AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel from a JSON string
ai_model_insights_summary_response_summary_weighted_visibility_by_model_instance = AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel.to_json())

# convert the object into a dict
ai_model_insights_summary_response_summary_weighted_visibility_by_model_dict = ai_model_insights_summary_response_summary_weighted_visibility_by_model_instance.to_dict()
# create an instance of AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel from a dict
ai_model_insights_summary_response_summary_weighted_visibility_by_model_from_dict = AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel.from_dict(ai_model_insights_summary_response_summary_weighted_visibility_by_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


