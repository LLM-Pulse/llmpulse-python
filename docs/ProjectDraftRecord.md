# ProjectDraftRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**draft_id** | **str** | Draft id (draft_...) | 
**status** | **str** | open, finalized or expired | 
**current_step** | **str** | The next step to submit (details, prompts, competitors, owned_media), or ready when the draft can be finalized | 
**steps_completed** | **List[str]** |  | 
**steps_remaining** | **List[str]** | Required steps not submitted yet | 
**optional_steps** | **List[str]** | Steps the plan allows but finalize does not require (owned_media from Growth) | 
**finalizable** | **bool** |  | 
**website_url** | **str** |  | 
**main_country** | **str** |  | 
**main_language** | **str** |  | 
**use_subdomain** | **bool** |  | 
**name** | **str** | Null until the details step | 
**brand_name** | **str** |  | 
**description** | **str** |  | 
**industry** | **List[str]** |  | 
**matching_names** | **List[str]** |  | 
**prompts** | **List[str]** |  | 
**competitors** | [**List[ProjectDraftRecordCompetitorsInner]**](ProjectDraftRecordCompetitorsInner.md) |  | 
**owned_media** | [**ProjectDraftRecordOwnedMedia**](ProjectDraftRecordOwnedMedia.md) |  | 
**weekly_email_subscribed** | **bool** |  | 
**external_identifier** | **str** |  | 
**execute_prompts_immediately** | **bool** |  | 
**project_id** | **int** | The project the draft became; null until finalized | 
**expires_at** | **datetime** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.project_draft_record import ProjectDraftRecord

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDraftRecord from a JSON string
project_draft_record_instance = ProjectDraftRecord.from_json(json)
# print the JSON string representation of the object
print(ProjectDraftRecord.to_json())

# convert the object into a dict
project_draft_record_dict = project_draft_record_instance.to_dict()
# create an instance of ProjectDraftRecord from a dict
project_draft_record_from_dict = ProjectDraftRecord.from_dict(project_draft_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


