# TechnicalGeoReportContentUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**report_type** | **str** | Always llms_txt | [optional] 
**project_id** | **int** |  | [optional] 
**batch_id** | **int** | Bundle the report was created in; null for a report created on its own | [optional] 
**url** | **str** | Always null for llms_txt reports; domain names the website | [optional] 
**domain** | **str** |  | [optional] 
**country_code** | **str** |  | [optional] 
**output_language_code** | **str** | ISO 639-1 code the files were requested in; null when they are written in the website&#39;s own language | [optional] 
**status** | **str** |  | [optional] 
**result_available** | **bool** |  | [optional] 
**overall_score** | **float** | Always null for llms_txt reports | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**result_data** | [**LlmsTxtTechnicalGeoReportResultData**](LlmsTxtTechnicalGeoReportResultData.md) |  | [optional] 
**error_message** | **str** |  | [optional] 
**poll_after_seconds** | **int** | Seconds to wait before polling again while the report runs; null once it has finished | [optional] 
**app_url** | **str** | Opens this report in the app | [optional] 
**request_id** | **str** |  | [optional] 
**changed_files** | **List[str]** | Files whose text actually changed; empty when every file matched the stored text | [optional] 

## Example

```python
from llmpulse.models.technical_geo_report_content_update_response import TechnicalGeoReportContentUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TechnicalGeoReportContentUpdateResponse from a JSON string
technical_geo_report_content_update_response_instance = TechnicalGeoReportContentUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(TechnicalGeoReportContentUpdateResponse.to_json())

# convert the object into a dict
technical_geo_report_content_update_response_dict = technical_geo_report_content_update_response_instance.to_dict()
# create an instance of TechnicalGeoReportContentUpdateResponse from a dict
technical_geo_report_content_update_response_from_dict = TechnicalGeoReportContentUpdateResponse.from_dict(technical_geo_report_content_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


