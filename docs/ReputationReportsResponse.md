# ReputationReportsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[ReputationReportSummary]**](ReputationReportSummary.md) |  | 

## Example

```python
from llmpulse.models.reputation_reports_response import ReputationReportsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ReputationReportsResponse from a JSON string
reputation_reports_response_instance = ReputationReportsResponse.from_json(json)
# print the JSON string representation of the object
print(ReputationReportsResponse.to_json())

# convert the object into a dict
reputation_reports_response_dict = reputation_reports_response_instance.to_dict()
# create an instance of ReputationReportsResponse from a dict
reputation_reports_response_from_dict = ReputationReportsResponse.from_dict(reputation_reports_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


