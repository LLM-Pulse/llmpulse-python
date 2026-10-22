# ProjectDetailsAllOfAgentTraffic

Agent traffic source behind /metrics/agent_traffic. connected and reconnect_required (the source refused the stored access, so syncing stopped) both answer from stored data; imported means no live source is connected but imported logs answer; not_connected means it returns ERR_AGENT_TRAFFIC_NOT_CONNECTED.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**provider** | **str** | The connected source (e.g. cloudflare_graphql, bunny_cdn, s3 or the log drain&#39;s provider), null without a live source | [optional] 
**connect_url** | **str** | The in-app Agent Analytics page, where a source is connected or reconnected | [optional] 

## Example

```python
from llmpulse.models.project_details_all_of_agent_traffic import ProjectDetailsAllOfAgentTraffic

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDetailsAllOfAgentTraffic from a JSON string
project_details_all_of_agent_traffic_instance = ProjectDetailsAllOfAgentTraffic.from_json(json)
# print the JSON string representation of the object
print(ProjectDetailsAllOfAgentTraffic.to_json())

# convert the object into a dict
project_details_all_of_agent_traffic_dict = project_details_all_of_agent_traffic_instance.to_dict()
# create an instance of ProjectDetailsAllOfAgentTraffic from a dict
project_details_all_of_agent_traffic_from_dict = ProjectDetailsAllOfAgentTraffic.from_dict(project_details_all_of_agent_traffic_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


