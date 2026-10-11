# RevokeTeamInvitation200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**revoked** | **bool** |  | [optional] 
**id** | **int** |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.revoke_team_invitation200_response import RevokeTeamInvitation200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RevokeTeamInvitation200Response from a JSON string
revoke_team_invitation200_response_instance = RevokeTeamInvitation200Response.from_json(json)
# print the JSON string representation of the object
print(RevokeTeamInvitation200Response.to_json())

# convert the object into a dict
revoke_team_invitation200_response_dict = revoke_team_invitation200_response_instance.to_dict()
# create an instance of RevokeTeamInvitation200Response from a dict
revoke_team_invitation200_response_from_dict = RevokeTeamInvitation200Response.from_dict(revoke_team_invitation200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


