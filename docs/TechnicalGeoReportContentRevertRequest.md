# TechnicalGeoReportContentRevertRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**report_type** | **str** | Only llms_txt reports have editable content | 

## Example

```python
from llmpulse.models.technical_geo_report_content_revert_request import TechnicalGeoReportContentRevertRequest

# TODO update the JSON string below
json = "{}"
# create an instance of TechnicalGeoReportContentRevertRequest from a JSON string
technical_geo_report_content_revert_request_instance = TechnicalGeoReportContentRevertRequest.from_json(json)
# print the JSON string representation of the object
print(TechnicalGeoReportContentRevertRequest.to_json())

# convert the object into a dict
technical_geo_report_content_revert_request_dict = technical_geo_report_content_revert_request_instance.to_dict()
# create an instance of TechnicalGeoReportContentRevertRequest from a dict
technical_geo_report_content_revert_request_from_dict = TechnicalGeoReportContentRevertRequest.from_dict(technical_geo_report_content_revert_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


