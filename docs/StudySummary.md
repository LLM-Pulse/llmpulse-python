# StudySummary

One custom AI study

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

## Example

```python
from llmpulse.models.study_summary import StudySummary

# TODO update the JSON string below
json = "{}"
# create an instance of StudySummary from a JSON string
study_summary_instance = StudySummary.from_json(json)
# print the JSON string representation of the object
print(StudySummary.to_json())

# convert the object into a dict
study_summary_dict = study_summary_instance.to_dict()
# create an instance of StudySummary from a dict
study_summary_from_dict = StudySummary.from_dict(study_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


