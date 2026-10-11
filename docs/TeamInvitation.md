# TeamInvitation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Kept by the member once they accept, when they move to GET /team_members. | 
**email** | **str** |  | 
**permission_role** | **str** |  | 
**account_role** | [**TeamAccountRole**](TeamAccountRole.md) |  | 
**permissions** | **Dict[str, List[str]]** | What the person can do, feature key to the verbs granted (read, create, update, delete), resolved from their role. Null for the account owner, who can do everything. | 
**account_admin** | **bool** |  | 
**billing_access** | **bool** |  | 
**all_projects** | **bool** |  | 
**project_ids** | **List[int]** |  | 
**invited_at** | **datetime** | When the invitation email was last sent. | [optional] 
**expires_at** | **datetime** | When the invitation link stops working. | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.team_invitation import TeamInvitation

# TODO update the JSON string below
json = "{}"
# create an instance of TeamInvitation from a JSON string
team_invitation_instance = TeamInvitation.from_json(json)
# print the JSON string representation of the object
print(TeamInvitation.to_json())

# convert the object into a dict
team_invitation_dict = team_invitation_instance.to_dict()
# create an instance of TeamInvitation from a dict
team_invitation_from_dict = TeamInvitation.from_dict(team_invitation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


