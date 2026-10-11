# TeamMember


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**email** | **str** |  | 
**name** | **str** |  | [optional] 
**role** | **str** | The account owner is listed first; everyone else who joined is a member. | 
**status** | **str** | A blocked member cannot sign in or use the API until unblocked in the app. | 
**permission_role** | **str** | Access level of a member: full_access, view_only, custom or account_role. Null for the owner. | 
**account_role** | [**TeamAccountRole**](TeamAccountRole.md) |  | 
**permissions** | **Dict[str, List[str]]** | What the person can do, feature key to the verbs granted (read, create, update, delete), resolved from their role. Null for the account owner, who can do everything. | 
**account_admin** | **bool** | A co-owner, who can manage the team. | 
**billing_access** | **bool** | Can open Billing and Plans (always true for the owner). | 
**all_projects** | **bool** | Has access to every project of the account, including future ones. | 
**project_ids** | **List[int]** | The projects a member is limited to; empty when all_projects is true. | 
**last_sign_in_at** | **datetime** |  | [optional] 
**joined_at** | **datetime** | When the member accepted the invitation; null for the owner and for members added without one. | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.team_member import TeamMember

# TODO update the JSON string below
json = "{}"
# create an instance of TeamMember from a JSON string
team_member_instance = TeamMember.from_json(json)
# print the JSON string representation of the object
print(TeamMember.to_json())

# convert the object into a dict
team_member_dict = team_member_instance.to_dict()
# create an instance of TeamMember from a dict
team_member_from_dict = TeamMember.from_dict(team_member_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


