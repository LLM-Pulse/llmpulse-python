# CreateReputationReportRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**recalculate** | **bool** | Use this month&#39;s one manual recalculation instead of returning the existing report | [optional] [default to False]

## Example

```python
from llmpulse.models.create_reputation_report_request import CreateReputationReportRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateReputationReportRequest from a JSON string
create_reputation_report_request_instance = CreateReputationReportRequest.from_json(json)
# print the JSON string representation of the object
print(CreateReputationReportRequest.to_json())

# convert the object into a dict
create_reputation_report_request_dict = create_reputation_report_request_instance.to_dict()
# create an instance of CreateReputationReportRequest from a dict
create_reputation_report_request_from_dict = CreateReputationReportRequest.from_dict(create_reputation_report_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


