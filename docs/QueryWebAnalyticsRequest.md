# QueryWebAnalyticsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**query** | **object** | The query in the provider&#39;s native format (see GET /web_analytics/schema): a JSON object for GA4, Adobe, Matomo, Plausible and Piano; for PostHog, {\&quot;query\&quot;: \&quot;&lt;HogQL&gt;\&quot;} or the HogQL string. Deliberately untyped so generated clients accept either shape. | 

## Example

```python
from llmpulse.models.query_web_analytics_request import QueryWebAnalyticsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of QueryWebAnalyticsRequest from a JSON string
query_web_analytics_request_instance = QueryWebAnalyticsRequest.from_json(json)
# print the JSON string representation of the object
print(QueryWebAnalyticsRequest.to_json())

# convert the object into a dict
query_web_analytics_request_dict = query_web_analytics_request_instance.to_dict()
# create an instance of QueryWebAnalyticsRequest from a dict
query_web_analytics_request_from_dict = QueryWebAnalyticsRequest.from_dict(query_web_analytics_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


