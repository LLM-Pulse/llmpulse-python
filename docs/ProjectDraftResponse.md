# ProjectDraftResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**draft** | [**ProjectDraftRecord**](ProjectDraftRecord.md) |  | 
**suggestions** | [**ProjectDraftSuggestions**](ProjectDraftSuggestions.md) |  | 
**limits** | [**ProjectDraftResponseLimits**](ProjectDraftResponseLimits.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.project_draft_response import ProjectDraftResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDraftResponse from a JSON string
project_draft_response_instance = ProjectDraftResponse.from_json(json)
# print the JSON string representation of the object
print(ProjectDraftResponse.to_json())

# convert the object into a dict
project_draft_response_dict = project_draft_response_instance.to_dict()
# create an instance of ProjectDraftResponse from a dict
project_draft_response_from_dict = ProjectDraftResponse.from_dict(project_draft_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


