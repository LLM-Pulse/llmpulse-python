# AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_sentiments** | **int** | Brand sentiment verdicts across the models | [optional] 
**models** | [**List[AiModelSentimentRow]**](AiModelSentimentRow.md) |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_summary_response_summary_brand_net_sentiment_by_model import AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel from a JSON string
ai_model_insights_summary_response_summary_brand_net_sentiment_by_model_instance = AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel.to_json())

# convert the object into a dict
ai_model_insights_summary_response_summary_brand_net_sentiment_by_model_dict = ai_model_insights_summary_response_summary_brand_net_sentiment_by_model_instance.to_dict()
# create an instance of AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel from a dict
ai_model_insights_summary_response_summary_brand_net_sentiment_by_model_from_dict = AiModelInsightsSummaryResponseSummaryBrandNetSentimentByModel.from_dict(ai_model_insights_summary_response_summary_brand_net_sentiment_by_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


