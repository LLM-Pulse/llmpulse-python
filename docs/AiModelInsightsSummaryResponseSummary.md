# AiModelInsightsSummaryResponseSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mentions_by_model** | [**AiModelInsightsSummaryResponseSummaryMentionsByModel**](AiModelInsightsSummaryResponseSummaryMentionsByModel.md) |  | [optional] 
**citations_by_model** | [**AiModelInsightsSummaryResponseSummaryCitationsByModel**](AiModelInsightsSummaryResponseSummaryCitationsByModel.md) |  | [optional] 
**brand_net_sentiment_by_model** | [**AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel**](AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel.md) |  | [optional] 
**weighted_visibility_by_model** | [**AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel**](AiModelInsightsSummaryResponseSummaryWeightedVisibilityByModel.md) |  | [optional] 
**mentions_market_share** | [**AiModelRateMatrix**](AiModelRateMatrix.md) |  | [optional] 
**citations_market_share** | [**AiModelRateMatrix**](AiModelRateMatrix.md) |  | [optional] 
**sentiment_market_share** | [**AiModelInsightsSummaryResponseSummarySentimentMarketShare**](AiModelInsightsSummaryResponseSummarySentimentMarketShare.md) |  | [optional] 
**weighted_visibility_market_share** | [**AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare**](AiModelInsightsSummaryResponseSummaryWeightedVisibilityMarketShare.md) |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_summary_response_summary import AiModelInsightsSummaryResponseSummary

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsSummaryResponseSummary from a JSON string
ai_model_insights_summary_response_summary_instance = AiModelInsightsSummaryResponseSummary.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsSummaryResponseSummary.to_json())

# convert the object into a dict
ai_model_insights_summary_response_summary_dict = ai_model_insights_summary_response_summary_instance.to_dict()
# create an instance of AiModelInsightsSummaryResponseSummary from a dict
ai_model_insights_summary_response_summary_from_dict = AiModelInsightsSummaryResponseSummary.from_dict(ai_model_insights_summary_response_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


