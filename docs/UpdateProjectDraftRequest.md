# UpdateProjectDraftRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**step** | **str** |  | 
**name** | **str** |  | [optional] 
**brand_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**industry** | **List[str]** |  | [optional] 
**matching_names** | **List[str]** | Brand-name variants used to detect mentions (details step). At most 50 names of up to 100 characters each; the step stores the list as sent, and finalize refuses a longer list or name with ERR_INVALID_PARAM (422) | [optional] 
**external_identifier** | **str** |  | [optional] 
**prompts** | **List[str]** |  | [optional] 
**competitors** | **List[object]** | Competitors step: objects {domain, brand_name, matching_names}, capped by plan. Each competitor&#39;s matching_names takes at most 50 names of up to 100 characters, checked at finalize like POST /projects | [optional] 
**youtube_channel_url** | **str** |  | [optional] 
**instagram_profile_url** | **str** |  | [optional] 
**facebook_page_url** | **str** |  | [optional] 
**tiktok_profile_url** | **str** |  | [optional] 
**app_store_url** | **str** |  | [optional] 
**google_play_url** | **str** |  | [optional] 
**suggest** | **bool** |  | [optional] [default to True]

## Example

```python
from llmpulse.models.update_project_draft_request import UpdateProjectDraftRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateProjectDraftRequest from a JSON string
update_project_draft_request_instance = UpdateProjectDraftRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateProjectDraftRequest.to_json())

# convert the object into a dict
update_project_draft_request_dict = update_project_draft_request_instance.to_dict()
# create an instance of UpdateProjectDraftRequest from a dict
update_project_draft_request_from_dict = UpdateProjectDraftRequest.from_dict(update_project_draft_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


