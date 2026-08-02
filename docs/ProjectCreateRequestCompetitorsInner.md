# ProjectCreateRequestCompetitorsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** |  | 
**brand_name** | **str** |  | [optional] 
**matching_names** | **List[str]** |  | [optional] 

## Example

```python
from llmpulse.models.project_create_request_competitors_inner import ProjectCreateRequestCompetitorsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateRequestCompetitorsInner from a JSON string
project_create_request_competitors_inner_instance = ProjectCreateRequestCompetitorsInner.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateRequestCompetitorsInner.to_json())

# convert the object into a dict
project_create_request_competitors_inner_dict = project_create_request_competitors_inner_instance.to_dict()
# create an instance of ProjectCreateRequestCompetitorsInner from a dict
project_create_request_competitors_inner_from_dict = ProjectCreateRequestCompetitorsInner.from_dict(project_create_request_competitors_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


