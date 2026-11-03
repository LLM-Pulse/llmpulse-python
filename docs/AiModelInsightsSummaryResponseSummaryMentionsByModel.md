# AiModelInsightsSummaryResponseSummaryMentionsByModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_mentions** | **int** | Brand mentions across the models | [optional] 
**models** | [**List[AiModelMentionsRow]**](AiModelMentionsRow.md) |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_summary_response_summary_mentions_by_model import AiModelInsightsSummaryResponseSummaryMentionsByModel

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsSummaryResponseSummaryMentionsByModel from a JSON string
ai_model_insights_summary_response_summary_mentions_by_model_instance = AiModelInsightsSummaryResponseSummaryMentionsByModel.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsSummaryResponseSummaryMentionsByModel.to_json())

# convert the object into a dict
ai_model_insights_summary_response_summary_mentions_by_model_dict = ai_model_insights_summary_response_summary_mentions_by_model_instance.to_dict()
# create an instance of AiModelInsightsSummaryResponseSummaryMentionsByModel from a dict
ai_model_insights_summary_response_summary_mentions_by_model_from_dict = AiModelInsightsSummaryResponseSummaryMentionsByModel.from_dict(ai_model_insights_summary_response_summary_mentions_by_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


