# ProjectDraftSuggestionsDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**description** | **str** |  | 
**industry** | **List[str]** |  | 
**matching_names** | **List[str]** |  | 

## Example

```python
from llmpulse.models.project_draft_suggestions_details import ProjectDraftSuggestionsDetails

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDraftSuggestionsDetails from a JSON string
project_draft_suggestions_details_instance = ProjectDraftSuggestionsDetails.from_json(json)
# print the JSON string representation of the object
print(ProjectDraftSuggestionsDetails.to_json())

# convert the object into a dict
project_draft_suggestions_details_dict = project_draft_suggestions_details_instance.to_dict()
# create an instance of ProjectDraftSuggestionsDetails from a dict
project_draft_suggestions_details_from_dict = ProjectDraftSuggestionsDetails.from_dict(project_draft_suggestions_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


