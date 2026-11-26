# ProjectDraftSuggestions

AI suggestions for a step. Only the key of the suggested step is sent, and only when status is ready

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**step** | **str** | The step the suggestions are for (details, prompts or competitors) | [optional] 
**status** | **str** | ready, none (not requested, or nothing cached yet) or failed | 
**details** | [**ProjectDraftSuggestionsDetails**](ProjectDraftSuggestionsDetails.md) |  | [optional] 
**prompts** | **List[str]** |  | [optional] 
**competitors** | [**List[ProjectDraftSuggestionsCompetitorsInner]**](ProjectDraftSuggestionsCompetitorsInner.md) |  | [optional] 

## Example

```python
from llmpulse.models.project_draft_suggestions import ProjectDraftSuggestions

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDraftSuggestions from a JSON string
project_draft_suggestions_instance = ProjectDraftSuggestions.from_json(json)
# print the JSON string representation of the object
print(ProjectDraftSuggestions.to_json())

# convert the object into a dict
project_draft_suggestions_dict = project_draft_suggestions_instance.to_dict()
# create an instance of ProjectDraftSuggestions from a dict
project_draft_suggestions_from_dict = ProjectDraftSuggestions.from_dict(project_draft_suggestions_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


