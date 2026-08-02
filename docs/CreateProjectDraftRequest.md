# CreateProjectDraftRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_url** | **str** | Public HTTP(S) URL with a DNS hostname or public IP address. Credentials, private and special IP addresses, localhost and internal hostnames are rejected. | 
**main_country** | **str** |  | 
**main_language** | **str** |  | 
**use_subdomain** | **bool** |  | [optional] [default to False]
**suggest** | **bool** |  | [optional] [default to True]
**execute_prompts_immediately** | **bool** |  | [optional] [default to True]

## Example

```python
from llmpulse.models.create_project_draft_request import CreateProjectDraftRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateProjectDraftRequest from a JSON string
create_project_draft_request_instance = CreateProjectDraftRequest.from_json(json)
# print the JSON string representation of the object
print(CreateProjectDraftRequest.to_json())

# convert the object into a dict
create_project_draft_request_dict = create_project_draft_request_instance.to_dict()
# create an instance of CreateProjectDraftRequest from a dict
create_project_draft_request_from_dict = CreateProjectDraftRequest.from_dict(create_project_draft_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


