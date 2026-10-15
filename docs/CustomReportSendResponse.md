# CustomReportSendResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**id** | **int** |  | 
**status** | **str** |  | 
**recipients_count** | **int** |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.custom_report_send_response import CustomReportSendResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CustomReportSendResponse from a JSON string
custom_report_send_response_instance = CustomReportSendResponse.from_json(json)
# print the JSON string representation of the object
print(CustomReportSendResponse.to_json())

# convert the object into a dict
custom_report_send_response_dict = custom_report_send_response_instance.to_dict()
# create an instance of CustomReportSendResponse from a dict
custom_report_send_response_from_dict = CustomReportSendResponse.from_dict(custom_report_send_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


