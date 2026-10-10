# WebAnalyticsSchemaResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**provider** | **str** | The connected web analytics provider. | [optional] 
**var_property** | **str** | The property, site, report suite (rsid:...), data view (dataview:...) or project every query runs on. | [optional] 
**query_language** | **str** | The native query format the provider accepts. | [optional] 
**docs_url** | **str** | The provider&#39;s reference for that format. | [optional] 
**allowed_fields** | **List[str]** | Top-level query fields that are forwarded. | [optional] 
**rules** | **List[str]** | What the bridge enforces and the provider&#39;s main constraints. | [optional] 
**example** | **Dict[str, object]** | A worked query to adapt. | [optional] 
**fields** | **Dict[str, object]** | The provider&#39;s live field list where it offers one: GA4 dimensions and metrics with custom definitions, Adobe ids, Matomo report methods, PostHog event names, the Plausible catalog. Null when the provider did not return it. | [optional] 
**fields_unavailable** | **str** | Present when the field list could not be read; the format and example still apply. | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.web_analytics_schema_response import WebAnalyticsSchemaResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebAnalyticsSchemaResponse from a JSON string
web_analytics_schema_response_instance = WebAnalyticsSchemaResponse.from_json(json)
# print the JSON string representation of the object
print(WebAnalyticsSchemaResponse.to_json())

# convert the object into a dict
web_analytics_schema_response_dict = web_analytics_schema_response_instance.to_dict()
# create an instance of WebAnalyticsSchemaResponse from a dict
web_analytics_schema_response_from_dict = WebAnalyticsSchemaResponse.from_dict(web_analytics_schema_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


