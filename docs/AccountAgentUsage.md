# AccountAgentUsage

The share of this calendar month's allowance for the in-app AI assistant (Europe/Madrid) that the account's team has used, owner and members together; each embedded project has an allowance of its own, left out here. The allowance is published as a share only, never as an amount; longer questions and bigger analyses use more of it. Deleting conversations gives nothing back.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**percent_used** | **int** | Whole percent used, rounded down, from 0 to 100; 100 means the allowance is spent and new questions wait until resets_on. null when unlimited is true | [optional] 
**unlimited** | **bool** |  | [optional] 
**included** | **bool** | Whether the plan includes the in-app AI assistant. false on a plan without it, where percent_used is 100 | [optional] 
**period** | **str** | Always month | [optional] 
**resets_on** | **date** | The first day of next month, when the allowance starts again | [optional] 

## Example

```python
from llmpulse.models.account_agent_usage import AccountAgentUsage

# TODO update the JSON string below
json = "{}"
# create an instance of AccountAgentUsage from a JSON string
account_agent_usage_instance = AccountAgentUsage.from_json(json)
# print the JSON string representation of the object
print(AccountAgentUsage.to_json())

# convert the object into a dict
account_agent_usage_dict = account_agent_usage_instance.to_dict()
# create an instance of AccountAgentUsage from a dict
account_agent_usage_from_dict = AccountAgentUsage.from_dict(account_agent_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


