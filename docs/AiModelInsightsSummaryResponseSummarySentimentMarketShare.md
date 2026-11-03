# AiModelInsightsSummaryResponseSummarySentimentMarketShare


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actors** | [**List[AiModelSentimentMatrixActor]**](AiModelSentimentMatrixActor.md) | The project and each competitor with a sentiment verdict in the window (only the competitors given in competitors, when it is given), by total_sentiments descending | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_summary_response_summary_sentiment_market_share import AiModelInsightsSummaryResponseSummarySentimentMarketShare

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsSummaryResponseSummarySentimentMarketShare from a JSON string
ai_model_insights_summary_response_summary_sentiment_market_share_instance = AiModelInsightsSummaryResponseSummarySentimentMarketShare.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsSummaryResponseSummarySentimentMarketShare.to_json())

# convert the object into a dict
ai_model_insights_summary_response_summary_sentiment_market_share_dict = ai_model_insights_summary_response_summary_sentiment_market_share_instance.to_dict()
# create an instance of AiModelInsightsSummaryResponseSummarySentimentMarketShare from a dict
ai_model_insights_summary_response_summary_sentiment_market_share_from_dict = AiModelInsightsSummaryResponseSummarySentimentMarketShare.from_dict(ai_model_insights_summary_response_summary_sentiment_market_share_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


