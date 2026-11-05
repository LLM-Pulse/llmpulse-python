# ReputationReportSummary

One reputation report's status and analyst model coverage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Report id for GET /reputation/reports/{id} | 
**status** | **str** |  | 
**created_at** | **datetime** |  | 
**processed_at** | **datetime** |  | [optional] 
**available_models** | **List[str]** | Analyst models that produced data | 
**missing_models** | **List[str]** | Analyst models with no data yet | 
**error_message** | **str** | Why the report failed; null unless status is failed | [optional] 

## Example

```python
from llmpulse.models.reputation_report_summary import ReputationReportSummary

# TODO update the JSON string below
json = "{}"
# create an instance of ReputationReportSummary from a JSON string
reputation_report_summary_instance = ReputationReportSummary.from_json(json)
# print the JSON string representation of the object
print(ReputationReportSummary.to_json())

# convert the object into a dict
reputation_report_summary_dict = reputation_report_summary_instance.to_dict()
# create an instance of ReputationReportSummary from a dict
reputation_report_summary_from_dict = ReputationReportSummary.from_dict(reputation_report_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


