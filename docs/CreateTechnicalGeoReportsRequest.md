# CreateTechnicalGeoReportsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**url** | **str** |  | 
**country_code** | **str** | Defaults to the project country | [optional] 
**output_language_code** | **str** | ISO 639-1 code of the language the llms.txt files are written in (for example es). Defaults to the project language, else en. Only the llms.txt report of the bundle uses it; an unsupported code returns 422 ERR_INVALID_PARAM | [optional] 

## Example

```python
from llmpulse.models.create_technical_geo_reports_request import CreateTechnicalGeoReportsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateTechnicalGeoReportsRequest from a JSON string
create_technical_geo_reports_request_instance = CreateTechnicalGeoReportsRequest.from_json(json)
# print the JSON string representation of the object
print(CreateTechnicalGeoReportsRequest.to_json())

# convert the object into a dict
create_technical_geo_reports_request_dict = create_technical_geo_reports_request_instance.to_dict()
# create an instance of CreateTechnicalGeoReportsRequest from a dict
create_technical_geo_reports_request_from_dict = CreateTechnicalGeoReportsRequest.from_dict(create_technical_geo_reports_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


