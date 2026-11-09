# CmsPublication


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**platform** | **str** |  | [optional] 
**site_url** | **str** |  | [optional] 
**status** | **str** | queued and sending are on their way; unknown means a send timed out and the next attempt looks the draft up before creating one; drafted carries remote_id and edit_url; failed carries error_code | [optional] 
**title** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**source_url** | **str** | For an update task, the page the draft revises | [optional] 
**remote_id** | **int** | WordPress post id of the draft | [optional] 
**remote_status** | **str** | WordPress status of the post when the draft was created (draft) | [optional] 
**remote_url** | **str** |  | [optional] 
**edit_url** | **str** | The post&#39;s edit screen in the WordPress admin | [optional] 
**error_code** | **str** | Why the send failed, the same token as error.meta.reason, for example reconnect_required, authorization_header_lost, missing_capability, firewall_blocked, timeout, unreachable or rejected | [optional] 
**created_at** | **datetime** |  | [optional] 
**sent_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.cms_publication import CmsPublication

# TODO update the JSON string below
json = "{}"
# create an instance of CmsPublication from a JSON string
cms_publication_instance = CmsPublication.from_json(json)
# print the JSON string representation of the object
print(CmsPublication.to_json())

# convert the object into a dict
cms_publication_dict = cms_publication_instance.to_dict()
# create an instance of CmsPublication from a dict
cms_publication_from_dict = CmsPublication.from_dict(cms_publication_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


