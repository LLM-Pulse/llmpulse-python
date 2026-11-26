# ProjectDraftResponseLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompts_available** | **int** | Prompts the account can still add; null when unlimited | 
**max_prompts_per_request** | **int** |  | 
**max_competitors** | **int** | Competitors the plan allows per project | 

## Example

```python
from llmpulse.models.project_draft_response_limits import ProjectDraftResponseLimits

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDraftResponseLimits from a JSON string
project_draft_response_limits_instance = ProjectDraftResponseLimits.from_json(json)
# print the JSON string representation of the object
print(ProjectDraftResponseLimits.to_json())

# convert the object into a dict
project_draft_response_limits_dict = project_draft_response_limits_instance.to_dict()
# create an instance of ProjectDraftResponseLimits from a dict
project_draft_response_limits_from_dict = ProjectDraftResponseLimits.from_dict(project_draft_response_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


