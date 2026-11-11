# AccountPitchQuota

Pitch projects created this calendar month (Europe/Madrid) against the monthly allowance, which pitch projects use instead of a project slot. limit and remaining are null when unlimited is true.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **int** |  | [optional] 
**used** | **int** |  | [optional] 
**remaining** | **int** |  | [optional] 
**unlimited** | **bool** |  | [optional] 
**period** | **str** | Always month | [optional] 
**resets_on** | **date** | The first day of next month, when the allowance starts again | [optional] 
**access** | **str** | Whether the account may create pitch projects, which are for agency and platform accounts (the account type, which the account owner or an account admin changes in Account Settings &gt; Profile). none means the account is not an agency; approved access goes dormant while the account is below the Scale tier, on a trial, has a payment problem, is set to cancel or has an allowance of 0; revoked means our team turned it off. pending and rejected are no longer returned | [optional] 

## Example

```python
from llmpulse.models.account_pitch_quota import AccountPitchQuota

# TODO update the JSON string below
json = "{}"
# create an instance of AccountPitchQuota from a JSON string
account_pitch_quota_instance = AccountPitchQuota.from_json(json)
# print the JSON string representation of the object
print(AccountPitchQuota.to_json())

# convert the object into a dict
account_pitch_quota_dict = account_pitch_quota_instance.to_dict()
# create an instance of AccountPitchQuota from a dict
account_pitch_quota_from_dict = AccountPitchQuota.from_dict(account_pitch_quota_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


