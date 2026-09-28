# ProjectCreateResponseCollectionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**prompts_attached** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.project_create_response_collections_inner import ProjectCreateResponseCollectionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateResponseCollectionsInner from a JSON string
project_create_response_collections_inner_instance = ProjectCreateResponseCollectionsInner.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateResponseCollectionsInner.to_json())

# convert the object into a dict
project_create_response_collections_inner_dict = project_create_response_collections_inner_instance.to_dict()
# create an instance of ProjectCreateResponseCollectionsInner from a dict
project_create_response_collections_inner_from_dict = ProjectCreateResponseCollectionsInner.from_dict(project_create_response_collections_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


