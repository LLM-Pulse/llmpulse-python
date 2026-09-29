# LlmsTxtTechnicalGeoReportResultData

The files and generation details once the report has completed; null before that

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**llms_txt_content** | **str** | Current llms.txt, manual edits included | [optional] 
**llms_full_txt_content** | **str** | Current llms-full.txt, manual edits included | [optional] 
**manually_edited_at** | **datetime** | When the files were last edited by hand in the app, the API or MCP; null while they are as generated | [optional] 
**content_version** | **str** | Send it back as content_version when editing the files. It changes on every save | [optional] 
**original_llms_txt_content** | **str** | The generated llms.txt, kept from the first manual edit; null while the files are as generated | [optional] 
**original_llms_full_txt_content** | **str** | The generated llms-full.txt, kept from the first manual edit; null while the files are as generated | [optional] 
**crawl_data** | **object** |  | [optional] 
**metadata** | **object** | Generation details, including output_language_code, the language the files were written in | [optional] 
**pages_crawled** | **int** |  | [optional] 
**generation_time_ms** | **int** |  | [optional] 
**openai_tokens_used** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.llms_txt_technical_geo_report_result_data import LlmsTxtTechnicalGeoReportResultData

# TODO update the JSON string below
json = "{}"
# create an instance of LlmsTxtTechnicalGeoReportResultData from a JSON string
llms_txt_technical_geo_report_result_data_instance = LlmsTxtTechnicalGeoReportResultData.from_json(json)
# print the JSON string representation of the object
print(LlmsTxtTechnicalGeoReportResultData.to_json())

# convert the object into a dict
llms_txt_technical_geo_report_result_data_dict = llms_txt_technical_geo_report_result_data_instance.to_dict()
# create an instance of LlmsTxtTechnicalGeoReportResultData from a dict
llms_txt_technical_geo_report_result_data_from_dict = LlmsTxtTechnicalGeoReportResultData.from_dict(llms_txt_technical_geo_report_result_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


