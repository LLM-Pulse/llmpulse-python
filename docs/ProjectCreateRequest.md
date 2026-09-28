# ProjectCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_url** | **str** | Public HTTP(S) URL with a DNS hostname or public IP address. Credentials, private and special IP addresses, localhost and internal hostnames are rejected. | 
**name** | **str** | Project name, as plain text. It can be changed later with PATCH /projects/{id} | 
**main_country** | **str** |  | 
**main_language** | **str** |  | 
**brand_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**industry** | **List[str]** | Industry keys, case-insensitive; a single key string is also accepted. An unknown key returns ERR_INVALID_PARAM listing the valid keys (the same list as the in-app industry picker, e.g. TECHNOLOGY, SAAS, ECOMMERCE) | [optional] 
**business_model** | **str** | Business model key (e.g. B2B_SAAS, MARKETPLACE); unknown keys are rejected | [optional] 
**business_model_other** | **str** | Free-text business model, only accepted when business_model is OTHER; rejected against any other key | [optional] 
**target_audience** | **str** | Who the brand sells to. Context for Recommendations and GEO Writer (Brand Book) | [optional] 
**brand_voice** | **str** | Tone of voice guidance for generated content (Brand Book) | [optional] 
**goals** | **str** | What the brand wants to achieve. Context for GEO Writer and prompt suggestions | [optional] 
**primary_products** | **List[str]** | Main products or services | [optional] 
**matching_names** | **List[str]** |  | [optional] 
**prompts** | **List[str]** |  | [optional] 
**collections** | [**List[ProjectCreateRequestCollectionsInner]**](ProjectCreateRequestCollectionsInner.md) | Collections (prompt tags) created with the project, each tagging prompts of this request by their exact text, so no separate tagging calls are needed. A text that is not in prompts returns ERR_INVALID_PARAM. A team member also needs Tags: Create permission. | [optional] 
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


