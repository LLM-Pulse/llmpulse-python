# ListTeamInvitations200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[TeamInvitation]**](TeamInvitation.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.list_team_invitations200_response import ListTeamInvitations200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListTeamInvitations200Response from a JSON string
list_team_invitations200_response_instance = ListTeamInvitations200Response.from_json(json)
# print the JSON string representation of the object
print(ListTeamInvitations200Response.to_json())

# convert the object into a dict
list_team_invitations200_response_dict = list_team_invitations200_response_instance.to_dict()
# create an instance of ListTeamInvitations200Response from a dict
list_team_invitations200_response_from_dict = ListTeamInvitations200Response.from_dict(list_team_invitations200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


