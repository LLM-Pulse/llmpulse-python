# ProjectCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project** | **object** | Same shape as GET /dimensions/projects/{id} | [optional] 
**prompts** | [**ProjectCreateResponsePrompts**](ProjectCreateResponsePrompts.md) |  | [optional] 
**competitors** | [**ProjectCreateResponseCompetitors**](ProjectCreateResponseCompetitors.md) |  | [optional] 
**collections** | [**List[ProjectCreateResponseCollectionsInner]**](ProjectCreateResponseCollectionsInner.md) | Collections created from the request&#39;s collections field (empty when none were sent; absent on an idempotent replay) | [optional] 
**same_domain_projects** | [**List[ProjectCreateResponseSameDomainProjectsInner]**](ProjectCreateResponseSameDomainProjectsInner.md) | Projects the caller can already see on the same domain (absent on an idempotent replay). Informational only: the create is never blocked, since one domain tracked per market is a normal setup. | [optional] 
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


