# TechnicalGeoReportsCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url** | **str** | The URL analysed | 
**country_code** | **str** | The country used, the project country when none was sent | 
**output_language_code** | **str** | ISO 639-1 code the llms.txt files are written in, or auto for the website&#39;s own language | 
**batch_id** | **int** | Bundle id, for the batch_id filter of GET /technical_geo_reports; null when no report was created | 
**created_reports** | **List[str]** | The report_type of every report created | 
**report_ids** | **Dict[str, int]** | The id of each created report, by report_type | 
**app_urls** | **Dict[str, str]** | The link that opens each created report in the app, by report_type | 
**failed_reports** | [**List[TechnicalGeoReportsCreateResponseFailedReportsInner]**](TechnicalGeoReportsCreateResponseFailedReportsInner.md) | Reports that could not be created, with the reasons | 
**next_endpoint** | **str** | Path template to poll each created report | 
**poll_after_seconds** | **int** | Seconds to wait before the first poll | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.technical_geo_reports_create_response import TechnicalGeoReportsCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TechnicalGeoReportsCreateResponse from a JSON string
technical_geo_reports_create_response_instance = TechnicalGeoReportsCreateResponse.from_json(json)
# print the JSON string representation of the object
print(TechnicalGeoReportsCreateResponse.to_json())

# convert the object into a dict
technical_geo_reports_create_response_dict = technical_geo_reports_create_response_instance.to_dict()
# create an instance of TechnicalGeoReportsCreateResponse from a dict
technical_geo_reports_create_response_from_dict = TechnicalGeoReportsCreateResponse.from_dict(technical_geo_reports_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


