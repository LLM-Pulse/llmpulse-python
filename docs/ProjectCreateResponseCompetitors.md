# ProjectCreateResponseCompetitors


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created** | **int** |  | [optional] 
**processing** | **bool** | Always false; competitors are ready when the project transaction commits. | [optional] 

## Example

```python
from llmpulse.models.project_create_response_competitors import ProjectCreateResponseCompetitors

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateResponseCompetitors from a JSON string
project_create_response_competitors_instance = ProjectCreateResponseCompetitors.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateResponseCompetitors.to_json())

# convert the object into a dict
project_create_response_competitors_dict = project_create_response_competitors_instance.to_dict()
# create an instance of ProjectCreateResponseCompetitors from a dict
project_create_response_competitors_from_dict = ProjectCreateResponseCompetitors.from_dict(project_create_response_competitors_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


