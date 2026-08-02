# ProjectCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_url** | **str** | Public HTTP(S) URL with a DNS hostname or public IP address. Credentials, private and special IP addresses, localhost and internal hostnames are rejected. | 
**name** | **str** |  | 
**main_country** | **str** |  | 
**main_language** | **str** |  | 
**brand_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**industry** | **List[str]** |  | [optional] 
**matching_names** | **List[str]** |  | [optional] 
**prompts** | **List[str]** |  | [optional] 
**competitors** | [**List[ProjectCreateRequestCompetitorsInner]**](ProjectCreateRequestCompetitorsInner.md) |  | [optional] 
**owned_media** | [**ProjectCreateRequestOwnedMedia**](ProjectCreateRequestOwnedMedia.md) |  | [optional] 
**use_subdomain** | **bool** |  | [optional] [default to False]
**weekly_email_subscribed** | **bool** |  | [optional] [default to False]
**external_identifier** | **str** | Embed-enabled (Enterprise) accounts only; other accounts receive ERR_PLAN_REQUIRED. Idempotency key and embed-session join key, unique per account | [optional] 
**execute_prompts_immediately** | **bool** |  | [optional] [default to True]

## Example

```python
from llmpulse.models.project_create_request import ProjectCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateRequest from a JSON string
project_create_request_instance = ProjectCreateRequest.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateRequest.to_json())

# convert the object into a dict
project_create_request_dict = project_create_request_instance.to_dict()
# create an instance of ProjectCreateRequest from a dict
project_create_request_from_dict = ProjectCreateRequest.from_dict(project_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


