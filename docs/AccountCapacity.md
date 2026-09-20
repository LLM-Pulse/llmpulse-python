# AccountCapacity

A ceiling with no usage counter attached. limit is null when unlimited is true.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **int** |  | [optional] 
**unlimited** | **bool** |  | [optional] 

## Example

```python
from llmpulse.models.account_capacity import AccountCapacity

# TODO update the JSON string below
json = "{}"
# create an instance of AccountCapacity from a JSON string
account_capacity_instance = AccountCapacity.from_json(json)
# print the JSON string representation of the object
print(AccountCapacity.to_json())

# convert the object into a dict
account_capacity_dict = account_capacity_instance.to_dict()
# create an instance of AccountCapacity from a dict
account_capacity_from_dict = AccountCapacity.from_dict(account_capacity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


