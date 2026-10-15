# SendCustomReportRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 

## Example

```python
from llmpulse.models.send_custom_report_request import SendCustomReportRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SendCustomReportRequest from a JSON string
send_custom_report_request_instance = SendCustomReportRequest.from_json(json)
# print the JSON string representation of the object
print(SendCustomReportRequest.to_json())

# convert the object into a dict
send_custom_report_request_dict = send_custom_report_request_instance.to_dict()
# create an instance of SendCustomReportRequest from a dict
send_custom_report_request_from_dict = SendCustomReportRequest.from_dict(send_custom_report_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


