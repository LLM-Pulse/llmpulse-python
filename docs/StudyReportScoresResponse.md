# StudyReportScoresResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**study_id** | **int** |  | 
**report** | [**ReputationReportSummary**](ReputationReportSummary.md) |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Score rows matching the filters across every page | 
**data** | [**List[AnalystScoreRow]**](AnalystScoreRow.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.study_report_scores_response import StudyReportScoresResponse

# TODO update the JSON string below
json = "{}"
# create an instance of StudyReportScoresResponse from a JSON string
study_report_scores_response_instance = StudyReportScoresResponse.from_json(json)
# print the JSON string representation of the object
print(StudyReportScoresResponse.to_json())

# convert the object into a dict
study_report_scores_response_dict = study_report_scores_response_instance.to_dict()
# create an instance of StudyReportScoresResponse from a dict
study_report_scores_response_from_dict = StudyReportScoresResponse.from_dict(study_report_scores_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


