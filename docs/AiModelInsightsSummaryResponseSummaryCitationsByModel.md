# AiModelInsightsSummaryResponseSummaryCitationsByModel


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_citations** | **int** | Citations of the brand&#39;s URLs across the models | [optional] 
**models** | [**List[AiModelCitationsRow]**](AiModelCitationsRow.md) |  | [optional] 

## Example

```python
from llmpulse.models.ai_model_insights_summary_response_summary_citations_by_model import AiModelInsightsSummaryResponseSummaryCitationsByModel

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelInsightsSummaryResponseSummaryCitationsByModel from a JSON string
ai_model_insights_summary_response_summary_citations_by_model_instance = AiModelInsightsSummaryResponseSummaryCitationsByModel.from_json(json)
# print the JSON string representation of the object
print(AiModelInsightsSummaryResponseSummaryCitationsByModel.to_json())

# convert the object into a dict
ai_model_insights_summary_response_summary_citations_by_model_dict = ai_model_insights_summary_response_summary_citations_by_model_instance.to_dict()
# create an instance of AiModelInsightsSummaryResponseSummaryCitationsByModel from a dict
ai_model_insights_summary_response_summary_citations_by_model_from_dict = AiModelInsightsSummaryResponseSummaryCitationsByModel.from_dict(ai_model_insights_summary_response_summary_citations_by_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


