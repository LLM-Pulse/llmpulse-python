# ProjectCreateRequestCollectionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**prompts** | **List[str]** |  | [optional] 

## Example

```python
from llmpulse.models.project_create_request_collections_inner import ProjectCreateRequestCollectionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateRequestCollectionsInner from a JSON string
project_create_request_collections_inner_instance = ProjectCreateRequestCollectionsInner.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateRequestCollectionsInner.to_json())

# convert the object into a dict
project_create_request_collections_inner_dict = project_create_request_collections_inner_instance.to_dict()
# create an instance of ProjectCreateRequestCollectionsInner from a dict
project_create_request_collections_inner_from_dict = ProjectCreateRequestCollectionsInner.from_dict(project_create_request_collections_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


