# AgentTrafficResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_from** | **date** |  | [optional] 
**to** | **date** |  | [optional] 
**group_by** | **str** |  | [optional] 
**granularity** | **str** |  | [optional] 
**totals** | **Dict[str, int]** |  | [optional] 
**timeseries** | **Dict[str, Dict[str, int]]** |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.agent_traffic_response import AgentTrafficResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AgentTrafficResponse from a JSON string
agent_traffic_response_instance = AgentTrafficResponse.from_json(json)
# print the JSON string representation of the object
print(AgentTrafficResponse.to_json())

# convert the object into a dict
agent_traffic_response_dict = agent_traffic_response_instance.to_dict()
# create an instance of AgentTrafficResponse from a dict
agent_traffic_response_from_dict = AgentTrafficResponse.from_dict(agent_traffic_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


