# AccountQuota

A consumable quota. limit and remaining are null when unlimited is true.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **int** |  | [optional] 
**used** | **int** |  | [optional] 
**remaining** | **int** |  | [optional] 
**unlimited** | **bool** |  | [optional] 
**period** | **str** | Reset window for quotas that reset (e.g. month) | [optional] 

## Example

```python
from llmpulse.models.account_quota import AccountQuota

# TODO update the JSON string below
json = "{}"
# create an instance of AccountQuota from a JSON string
account_quota_instance = AccountQuota.from_json(json)
# print the JSON string representation of the object
print(AccountQuota.to_json())

# convert the object into a dict
account_quota_dict = account_quota_instance.to_dict()
# create an instance of AccountQuota from a dict
account_quota_from_dict = AccountQuota.from_dict(account_quota_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


