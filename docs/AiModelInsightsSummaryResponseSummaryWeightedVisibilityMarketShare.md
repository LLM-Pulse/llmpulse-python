# AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actors** | [**List[AiModelWeightedVisibilityMatrixActor]**](AiModelWeightedVisibilityMatrixActor.md) | The project and each competitor with an AI Visibility Score in the window, 0 included (only the competitors given in competitors, when it is given), by total_weighted_visibility_score descending | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_summary_response_summary_weighted_visibility_market_share import AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare from a JSON string
ai_model_insights_summary_response_summary_weighted_visibility_market_share_instance = AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare.to_json())

# convert the object into a dict
ai_model_insights_summary_response_summary_weighted_visibility_market_share_dict = ai_model_insights_summary_response_summary_weighted_visibility_market_share_instance.to_dict()
# create an instance of AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare from a dict
ai_model_insights_summary_response_summary_weighted_visibility_market_share_from_dict = AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare.from_dict(ai_model_insights_summary_response_summary_weighted_visibility_market_share_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


