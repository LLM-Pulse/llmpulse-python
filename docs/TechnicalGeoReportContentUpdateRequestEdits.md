# TechnicalGeoReportContentUpdateRequestEdits

The files to replace, each mapped to its full replacement text: never blank, at most 200,000 characters. Send one file or both; a file identical to the stored one is ignored.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**llms_txt** | **str** | Full text of llms.txt | [optional] 
**llms_full_txt** | **str** | Full text of llms-full.txt | [optional] 

## Example

```python
from llmpulse.models.technical_geo_report_content_update_request_edits import TechnicalGeoReportContentUpdateRequestEdits

# TODO update the JSON string below
json = "{}"
# create an instance of TechnicalGeoReportContentUpdateRequestEdits from a JSON string
technical_geo_report_content_update_request_edits_instance = TechnicalGeoReportContentUpdateRequestEdits.from_json(json)
# print the JSON string representation of the object
print(TechnicalGeoReportContentUpdateRequestEdits.to_json())

# convert the object into a dict
technical_geo_report_content_update_request_edits_dict = technical_geo_report_content_update_request_edits_instance.to_dict()
# create an instance of TechnicalGeoReportContentUpdateRequestEdits from a dict
technical_geo_report_content_update_request_edits_from_dict = TechnicalGeoReportContentUpdateRequestEdits.from_dict(technical_geo_report_content_update_request_edits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


