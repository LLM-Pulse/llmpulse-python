# AgentBotsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bots** | [**List[AgentBot]**](AgentBot.md) |  | [optional] 
**companies** | **List[str]** |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.agent_bots_response import AgentBotsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AgentBotsResponse from a JSON string
agent_bots_response_instance = AgentBotsResponse.from_json(json)
# print the JSON string representation of the object
print(AgentBotsResponse.to_json())

# convert the object into a dict
agent_bots_response_dict = agent_bots_response_instance.to_dict()
# create an instance of AgentBotsResponse from a dict
agent_bots_response_from_dict = AgentBotsResponse.from_dict(agent_bots_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


