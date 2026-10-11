# TeamAccountRole

The account role the person follows, when permission_role is account_role; null otherwise.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 

## Example

```python
from llmpulse.models.team_account_role import TeamAccountRole

# TODO update the JSON string below
json = "{}"
# create an instance of TeamAccountRole from a JSON string
team_account_role_instance = TeamAccountRole.from_json(json)
# print the JSON string representation of the object
print(TeamAccountRole.to_json())

# convert the object into a dict
team_account_role_dict = team_account_role_instance.to_dict()
# create an instance of TeamAccountRole from a dict
team_account_role_from_dict = TeamAccountRole.from_dict(team_account_role_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


