# FinalizeProjectDraftRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**weekly_email_subscribed** | **bool** |  | [optional] 
**execute_prompts_immediately** | **bool** |  | [optional] 

## Example

```python
from llmpulse.models.finalize_project_draft_request import FinalizeProjectDraftRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FinalizeProjectDraftRequest from a JSON string
finalize_project_draft_request_instance = FinalizeProjectDraftRequest.from_json(json)
# print the JSON string representation of the object
print(FinalizeProjectDraftRequest.to_json())

# convert the object into a dict
finalize_project_draft_request_dict = finalize_project_draft_request_instance.to_dict()
# create an instance of FinalizeProjectDraftRequest from a dict
finalize_project_draft_request_from_dict = FinalizeProjectDraftRequest.from_dict(finalize_project_draft_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


