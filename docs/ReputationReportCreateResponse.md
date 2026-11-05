# ReputationReportCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**created** | **bool** | True when this request started a new report; false when it returned the one that already holds the month | 
**report** | [**ReputationReportSummary**](ReputationReportSummary.md) |  | 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.reputation_report_create_response import ReputationReportCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ReputationReportCreateResponse from a JSON string
reputation_report_create_response_instance = ReputationReportCreateResponse.from_json(json)
# print the JSON string representation of the object
print(ReputationReportCreateResponse.to_json())

# convert the object into a dict
reputation_report_create_response_dict = reputation_report_create_response_instance.to_dict()
# create an instance of ReputationReportCreateResponse from a dict
reputation_report_create_response_from_dict = ReputationReportCreateResponse.from_dict(reputation_report_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


