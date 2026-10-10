# WebAnalyticsQueryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**provider** | **str** |  | [optional] 
**var_property** | **str** |  | [optional] 
**columns** | [**List[WebAnalyticsQueryResponseColumnsInner]**](WebAnalyticsQueryResponseColumnsInner.md) |  | [optional] 
**rows** | **List[List[object]]** | One array per row, values in column order: strings, numbers or null. | [optional] 
**row_count** | **int** | Rows in this response (at most 5,000). | [optional] 
**total_rows** | **int** | Rows the provider has for the query, when it reports it. | [optional] 
**truncated** | **bool** | True when the provider has more rows than returned; page with its own offset or page field. | [optional] 
**totals** | **Dict[str, object]** | Metric totals by metric name, when the query asked for them. | [optional] 
**notes** | **List[str]** | Provider caveats: sampling, thresholds, more rows available. | [optional] 
**meta** | **Dict[str, object]** | Provider metadata such as GA4 time zone, currency and remaining property quota. | [optional] 
**fetched_at** | **datetime** | When the provider answered. | [optional] 
**cached** | **bool** | True when the answer came from the 10-minute cache instead of the provider. | [optional] 
**query** | **Dict[str, object]** | The request as sent to the provider, with the connected property forced and limits applied. | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.web_analytics_query_response import WebAnalyticsQueryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebAnalyticsQueryResponse from a JSON string
web_analytics_query_response_instance = WebAnalyticsQueryResponse.from_json(json)
# print the JSON string representation of the object
print(WebAnalyticsQueryResponse.to_json())

# convert the object into a dict
web_analytics_query_response_dict = web_analytics_query_response_instance.to_dict()
# create an instance of WebAnalyticsQueryResponse from a dict
web_analytics_query_response_from_dict = WebAnalyticsQueryResponse.from_dict(web_analytics_query_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


