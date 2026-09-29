# TechnicalGeoReportContentUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**report_type** | **str** | Only llms_txt reports have editable content | 
**content_version** | **str** | result_data.content_version of the report as last read. It changes on every save; a value that no longer matches is refused as stale | 
**edits** | [**TechnicalGeoReportContentUpdateRequestEdits**](TechnicalGeoReportContentUpdateRequestEdits.md) |  | 

## Example

```python
from llmpulse.models.technical_geo_report_content_update_request import TechnicalGeoReportContentUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of TechnicalGeoReportContentUpdateRequest from a JSON string
technical_geo_report_content_update_request_instance = TechnicalGeoReportContentUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(TechnicalGeoReportContentUpdateRequest.to_json())

# convert the object into a dict
technical_geo_report_content_update_request_dict = technical_geo_report_content_update_request_instance.to_dict()
# create an instance of TechnicalGeoReportContentUpdateRequest from a dict
technical_geo_report_content_update_request_from_dict = TechnicalGeoReportContentUpdateRequest.from_dict(technical_geo_report_content_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


