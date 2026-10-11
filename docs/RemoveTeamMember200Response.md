# RemoveTeamMember200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**removed** | **bool** |  | [optional] 
**id** | **int** |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.remove_team_member200_response import RemoveTeamMember200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RemoveTeamMember200Response from a JSON string
remove_team_member200_response_instance = RemoveTeamMember200Response.from_json(json)
# print the JSON string representation of the object
print(RemoveTeamMember200Response.to_json())

# convert the object into a dict
remove_team_member200_response_dict = remove_team_member200_response_instance.to_dict()
# create an instance of RemoveTeamMember200Response from a dict
remove_team_member200_response_from_dict = RemoveTeamMember200Response.from_dict(remove_team_member200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


