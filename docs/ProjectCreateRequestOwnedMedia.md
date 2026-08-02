# ProjectCreateRequestOwnedMedia

Requires Growth plan or above

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**youtube_channel_url** | **str** |  | [optional] 
**instagram_profile_url** | **str** |  | [optional] 
**facebook_page_url** | **str** |  | [optional] 
**tiktok_profile_url** | **str** |  | [optional] 
**app_store_url** | **str** |  | [optional] 
**google_play_url** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.project_create_request_owned_media import ProjectCreateRequestOwnedMedia

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectCreateRequestOwnedMedia from a JSON string
project_create_request_owned_media_instance = ProjectCreateRequestOwnedMedia.from_json(json)
# print the JSON string representation of the object
print(ProjectCreateRequestOwnedMedia.to_json())

# convert the object into a dict
project_create_request_owned_media_dict = project_create_request_owned_media_instance.to_dict()
# create an instance of ProjectCreateRequestOwnedMedia from a dict
project_create_request_owned_media_from_dict = ProjectCreateRequestOwnedMedia.from_dict(project_create_request_owned_media_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


