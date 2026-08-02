# AgentBot


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**company** | **str** |  | [optional] 
**category** | **str** |  | [optional] 
**cf_verified_category** | **str** |  | [optional] 
**description** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.agent_bot import AgentBot

# TODO update the JSON string below
json = "{}"
# create an instance of AgentBot from a JSON string
agent_bot_instance = AgentBot.from_json(json)
# print the JSON string representation of the object
print(AgentBot.to_json())

# convert the object into a dict
agent_bot_dict = agent_bot_instance.to_dict()
# create an instance of AgentBot from a dict
agent_bot_from_dict = AgentBot.from_dict(agent_bot_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


