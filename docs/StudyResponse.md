# StudyResponse

One custom AI study with its brief, subjects, dimensions and latest reports

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**title** | **str** |  | 
**study_type** | **str** | brand_set, sector, geo, topic or custom | 
**cadence** | **str** | one_shot or monthly | 
**status** | **str** | active or archived | 
**project_id** | **int** | The project the study is attached to; null for an account-level study | 
**subjects_count** | **int** |  | 
**ai_models** | **List[str]** | Analyst models the study runs on | 
**output_language_code** | **str** | ISO 639-1 code of the language the reports are written in | 
**created_at** | **datetime** |  | 
**last_report_at** | **datetime** | When the latest report started; null before the first one | 
**brief** | **str** | What the study asks the analyst models; null when none was written | 
**subjects** | **List[str]** | Names of the subjects it compares | 
**dimensions** | **List[str]** | Keys of the dimensions it scores, as the dimension filter takes them | 
**reports** | [**List[ReputationReportSummary]**](ReputationReportSummary.md) | The 24 latest reports, newest first | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.study_response import StudyResponse

# TODO update the JSON string below
json = "{}"
# create an instance of StudyResponse from a JSON string
study_response_instance = StudyResponse.from_json(json)
# print the JSON string representation of the object
print(StudyResponse.to_json())

# convert the object into a dict
study_response_dict = study_response_instance.to_dict()
# create an instance of StudyResponse from a dict
study_response_from_dict = StudyResponse.from_dict(study_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


