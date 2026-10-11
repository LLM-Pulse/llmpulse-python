# CreateTeamInvitationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**project_ids** | **List[int]** | Projects the member can access. Send this or all_projects true. | [optional] 
**all_projects** | **bool** | Access to every project, including future ones | [optional] 
**permission_role** | **str** | Default full_access. Owner and co-owners only. | [optional] 
**account_role_id** | **int** | One of the account&#39;s roles, with permission_role account_role | [optional] 
**permissions** | **Dict[str, List[str]]** | With permission_role custom: feature key to the verbs granted (read, create, update, delete), for example {\&quot;overview\&quot;: [\&quot;read\&quot;], \&quot;prompts\&quot;: [\&quot;read\&quot;, \&quot;create\&quot;]} | [optional] 
**account_admin** | **bool** | Make the member a co-owner. Account owner only. | [optional] 
**billing_access** | **bool** | Access to Billing and Plans. Account owner only. | [optional] 

## Example

```python
from llmpulse.models.create_team_invitation_request import CreateTeamInvitationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateTeamInvitationRequest from a JSON string
create_team_invitation_request_instance = CreateTeamInvitationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateTeamInvitationRequest.to_json())

# convert the object into a dict
create_team_invitation_request_dict = create_team_invitation_request_instance.to_dict()
# create an instance of CreateTeamInvitationRequest from a dict
create_team_invitation_request_from_dict = CreateTeamInvitationRequest.from_dict(create_team_invitation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


