# ProjectCreateResponsePrompts


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created** | **int** |  | [optional] 
**skipped** | **int** |  | [optional] 
**execution** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.project_create_response_prompts import ProjectCreateResponsePrompts

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateResponsePrompts from a JSON string
project_create_response_prompts_instance = ProjectCreateResponsePrompts.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateResponsePrompts.to_json())

# convert the object into a dict
project_create_response_prompts_dict = project_create_response_prompts_instance.to_dict()
# create an instance of ProjectCreateResponsePrompts from a dict
project_create_response_prompts_from_dict = ProjectCreateResponsePrompts.from_dict(project_create_response_prompts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


