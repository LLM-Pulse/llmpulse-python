# TechnicalGeoReportResponse

One technical GEO report with its result

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**report_type** | **str** | The report_type requested (agent_readiness for ai_readiness) | 
**project_id** | **int** |  | 
**batch_id** | **int** | Bundle the report was created in; null for a report created on its own | 
**url** | **str** | The page analysed; null for the domain-level types (robots_txt, agent_readiness, llms_txt, ai_visibility) | 
**domain** | **str** |  | 
**country_code** | **str** | Set only on llms_txt and ai_visibility reports | 
**output_language_code** | **str** | ISO 639-1 code an llms_txt report was requested in; null for an llms_txt report written in the website&#39;s own language and for every other type | 
**status** | **str** | Depends on report_type. Every type ends completed or failed; ai_visibility can also end insufficient_data | 
**result_available** | **bool** | Whether status is completed | 
**overall_score** | **float** | Null until the report completes, and always for llms_txt | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**result_data** | **Dict[str, object]** | The full result once the report has completed; null before that. Its shape depends on report_type; an llms_txt report returns its files as LlmsTxtTechnicalGeoReport describes | 
**error_message** | **str** | Why the report failed, or why an ai_visibility report found insufficient data; null otherwise | 
**poll_after_seconds** | **int** | Seconds to wait before polling again while the report runs; null once it has finished | 
**app_url** | **str** | Opens this report in the app | [optional] 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.technical_geo_report_response import TechnicalGeoReportResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TechnicalGeoReportResponse from a JSON string
technical_geo_report_response_instance = TechnicalGeoReportResponse.from_json(json)
# print the JSON string representation of the object
print(TechnicalGeoReportResponse.to_json())

# convert the object into a dict
technical_geo_report_response_dict = technical_geo_report_response_instance.to_dict()
# create an instance of TechnicalGeoReportResponse from a dict
technical_geo_report_response_from_dict = TechnicalGeoReportResponse.from_dict(technical_geo_report_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


