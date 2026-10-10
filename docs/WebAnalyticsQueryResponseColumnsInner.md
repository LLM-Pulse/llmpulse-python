# WebAnalyticsQueryResponseColumnsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**kind** | **str** | dimension or metric, when the provider says. | [optional] 
**type** | **str** | The provider&#39;s column type, when it says (PostHog). | [optional] 
**label** | **str** | The provider&#39;s display label, when it sends one (Piano). | [optional] 

## Example

```python
from llmpulse.models.web_analytics_query_response_columns_inner import WebAnalyticsQueryResponseColumnsInner

# TODO update the JSON string below
json = "{}"
# create an instance of WebAnalyticsQueryResponseColumnsInner from a JSON string
web_analytics_query_response_columns_inner_instance = WebAnalyticsQueryResponseColumnsInner.from_json(json)
# print the JSON string representation of the object
print(WebAnalyticsQueryResponseColumnsInner.to_json())

# convert the object into a dict
web_analytics_query_response_columns_inner_dict = web_analytics_query_response_columns_inner_instance.to_dict()
# create an instance of WebAnalyticsQueryResponseColumnsInner from a dict
web_analytics_query_response_columns_inner_from_dict = WebAnalyticsQueryResponseColumnsInner.from_dict(web_analytics_query_response_columns_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


