# ProjectCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project** | **object** | Same shape as GET /dimensions/projects/{id} | [optional] 
**prompts** | [**ProjectCreateResponsePrompts**](ProjectCreateResponsePrompts.md) |  | [optional] 
**competitors** | [**ProjectCreateResponseCompetitors**](ProjectCreateResponseCompetitors.md) |  | [optional] 
**email_subscription** | [**ProjectCreateResponseEmailSubscription**](ProjectCreateResponseEmailSubscription.md) |  | [optional] 
**limits** | [**ProjectCreateResponseLimits**](ProjectCreateResponseLimits.md) |  | [optional] 
**idempotent** | **bool** | Present and true only on external_identifier replays | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.project_create_response import ProjectCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateResponse from a JSON string
project_create_response_instance = ProjectCreateResponse.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateResponse.to_json())

# convert the object into a dict
project_create_response_dict = project_create_response_instance.to_dict()
# create an instance of ProjectCreateResponse from a dict
project_create_response_from_dict = ProjectCreateResponse.from_dict(project_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


