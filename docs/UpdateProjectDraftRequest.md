# UpdateProjectDraftRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**step** | **str** |  | 
**name** | **str** |  | [optional] 
**brand_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**industry** | **List[str]** |  | [optional] 
**matching_names** | **List[str]** |  | [optional] 
**external_identifier** | **str** |  | [optional] 
**prompts** | **List[str]** |  | [optional] 
**competitors** | **List[object]** |  | [optional] 
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


