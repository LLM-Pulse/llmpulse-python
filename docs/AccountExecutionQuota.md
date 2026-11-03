# AccountExecutionQuota

The account's allowance of AI answers for the current tracking window: its prompt limit times its enabled AI models, plus 5% so prompts can be replaced during the window. Every scheduled run and every first run of a new prompt spends one answer per AI model, and deleting a prompt gives nothing back. When it is used up, new prompts wait until resets_at. limit and remaining are null when unlimited is true. For a key limited to some projects, only remaining and unlimited (the account-wide answers left), period and resets_at.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **int** |  | [optional] 
**used** | **int** |  | [optional] 
**remaining** | **int** |  | [optional] 
**unlimited** | **bool** |  | [optional] 
**period** | **str** | The tracking window, from the account&#39;s tracking cadence (week runs Monday to Sunday) | [optional] 
**resets_at** | **datetime** | When the next window starts and the allowance is full again (00:00 Europe/Madrid) | [optional] 

## Example

```python
from llmpulse.models.account_execution_quota import AccountExecutionQuota

# TODO update the JSON string below
json = "{}"
# create an instance of AccountExecutionQuota from a JSON string
account_execution_quota_instance = AccountExecutionQuota.from_json(json)
# print the JSON string representation of the object
print(AccountExecutionQuota.to_json())

# convert the object into a dict
account_execution_quota_dict = account_execution_quota_instance.to_dict()
# create an instance of AccountExecutionQuota from a dict
account_execution_quota_from_dict = AccountExecutionQuota.from_dict(account_execution_quota_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


