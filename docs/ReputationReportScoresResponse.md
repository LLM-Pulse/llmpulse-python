# ReputationReportScoresResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**report** | [**ReputationReportSummary**](ReputationReportSummary.md) |  | 
**data** | [**List[AnalystScoreRow]**](AnalystScoreRow.md) |  | 

## Example

```python
from llmpulse.models.reputation_report_scores_response import ReputationReportScoresResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ReputationReportScoresResponse from a JSON string
reputation_report_scores_response_instance = ReputationReportScoresResponse.from_json(json)
# print the JSON string representation of the object
print(ReputationReportScoresResponse.to_json())

# convert the object into a dict
reputation_report_scores_response_dict = reputation_report_scores_response_instance.to_dict()
# create an instance of ReputationReportScoresResponse from a dict
reputation_report_scores_response_from_dict = ReputationReportScoresResponse.from_dict(reputation_report_scores_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


