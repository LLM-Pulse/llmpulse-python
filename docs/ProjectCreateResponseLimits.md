# ProjectCreateResponseLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**projects_remaining** | **int** |  | [optional] 
**prompts_available** | **int** |  | [optional] 
**competitors_remaining** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.project_create_response_limits import ProjectCreateResponseLimits

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateResponseLimits from a JSON string
project_create_response_limits_instance = ProjectCreateResponseLimits.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateResponseLimits.to_json())

# convert the object into a dict
project_create_response_limits_dict = project_create_response_limits_instance.to_dict()
# create an instance of ProjectCreateResponseLimits from a dict
project_create_response_limits_from_dict = ProjectCreateResponseLimits.from_dict(project_create_response_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


