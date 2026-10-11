# ListTeamMembers200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[TeamMember]**](TeamMember.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.list_team_members200_response import ListTeamMembers200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListTeamMembers200Response from a JSON string
list_team_members200_response_instance = ListTeamMembers200Response.from_json(json)
# print the JSON string representation of the object
print(ListTeamMembers200Response.to_json())

# convert the object into a dict
list_team_members200_response_dict = list_team_members200_response_instance.to_dict()
# create an instance of ListTeamMembers200Response from a dict
list_team_members200_response_from_dict = ListTeamMembers200Response.from_dict(list_team_members200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


