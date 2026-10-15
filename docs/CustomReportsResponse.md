# CustomReportsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[CustomReportSummary]**](CustomReportSummary.md) |  | 

## Example

```python
from llmpulse.models.custom_reports_response import CustomReportsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportsResponse from a JSON string
custom_reports_response_instance = CustomReportsResponse.from_json(json)
# print the JSON string representation of the object
print(CustomReportsResponse.to_json())

# convert the object into a dict
custom_reports_response_dict = custom_reports_response_instance.to_dict()
# create an instance of CustomReportsResponse from a dict
custom_reports_response_from_dict = CustomReportsResponse.from_dict(custom_reports_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


