# ProjectUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project** | [**ProjectProfile**](ProjectProfile.md) |  | 
**updated_fields** | **List[str]** | The fields the request sent | 
**rematching** | **bool** | True when a matching_names or additional_owned_domains change started a background recalculation of past answers; further edits are rejected until it finishes | 
**note** | **str** | What the change does to mention detection, citation ownership and historical numbers | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.project_update_response import ProjectUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectUpdateResponse from a JSON string
project_update_response_instance = ProjectUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(ProjectUpdateResponse.to_json())

# convert the object into a dict
project_update_response_dict = project_update_response_instance.to_dict()
# create an instance of ProjectUpdateResponse from a dict
project_update_response_from_dict = ProjectUpdateResponse.from_dict(project_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


