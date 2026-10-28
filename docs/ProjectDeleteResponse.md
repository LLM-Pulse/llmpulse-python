# ProjectDeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**deleted** | **bool** | Always true | 
**name** | **str** | The deleted project&#39;s name | 
**url** | **str** | The deleted project&#39;s website | 
**note** | **str** | What happens next; the deletion cannot be undone | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.project_delete_response import ProjectDeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDeleteResponse from a JSON string
project_delete_response_instance = ProjectDeleteResponse.from_json(json)
# print the JSON string representation of the object
print(ProjectDeleteResponse.to_json())

# convert the object into a dict
project_delete_response_dict = project_delete_response_instance.to_dict()
# create an instance of ProjectDeleteResponse from a dict
project_delete_response_from_dict = ProjectDeleteResponse.from_dict(project_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


