# ProjectDetailsAllOfAiTraffic

Web analytics provider behind /metrics/ai_traffic and /web_analytics. connected means both answer; reconnect_required means the provider refused the stored access, so /metrics/ai_traffic still answers from synced data and /web_analytics returns ERR_WEB_ANALYTICS_ACCESS_REVOKED until it is reconnected at connect_url; not_connected means they return ERR_AI_TRAFFIC_NOT_CONNECTED and ERR_WEB_ANALYTICS_NOT_CONNECTED.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**provider** | **str** | The connected provider (e.g. google_analytics, adobe_analytics, adobe_cja, posthog, plausible, matomo, piano), null when not connected | [optional] 
**connect_url** | **str** | The in-app AI Traffic page, where the provider is connected or reconnected | [optional] 

## Example

```python
from llmpulse.models.project_details_all_of_ai_traffic import ProjectDetailsAllOfAiTraffic

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDetailsAllOfAiTraffic from a JSON string
project_details_all_of_ai_traffic_instance = ProjectDetailsAllOfAiTraffic.from_json(json)
# print the JSON string representation of the object
print(ProjectDetailsAllOfAiTraffic.to_json())

# convert the object into a dict
project_details_all_of_ai_traffic_dict = project_details_all_of_ai_traffic_instance.to_dict()
# create an instance of ProjectDetailsAllOfAiTraffic from a dict
project_details_all_of_ai_traffic_from_dict = ProjectDetailsAllOfAiTraffic.from_dict(project_details_all_of_ai_traffic_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


