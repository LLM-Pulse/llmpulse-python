# OwnedMediaProfileSettings

The current value of every field PATCH /projects/{id}/owned_media accepts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**youtube_channel_url** | **str** |  | [optional] 
**app_store_url** | **str** |  | [optional] 
**google_play_url** | **str** |  | [optional] 
**instagram_profile_url** | **str** |  | [optional] 
**facebook_page_url** | **str** |  | [optional] 
**tiktok_profile_url** | **str** |  | [optional] 
**linkedin_company_url** | **str** |  | [optional] 
**youtube_extra_profile_urls** | **List[str]** |  | [optional] 
**mobile_apps_extra_profile_urls** | **List[str]** |  | [optional] 
**instagram_extra_profile_urls** | **List[str]** |  | [optional] 
**facebook_extra_profile_urls** | **List[str]** |  | [optional] 
**tiktok_extra_profile_urls** | **List[str]** |  | [optional] 
**linkedin_extra_profile_urls** | **List[str]** |  | [optional] 
**reddit_subreddits** | **List[str]** |  | [optional] 
**reddit_usernames** | **List[str]** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_profile_settings import OwnedMediaProfileSettings

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaProfileSettings from a JSON string
owned_media_profile_settings_instance = OwnedMediaProfileSettings.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaProfileSettings.to_json())

# convert the object into a dict
owned_media_profile_settings_dict = owned_media_profile_settings_instance.to_dict()
# create an instance of OwnedMediaProfileSettings from a dict
owned_media_profile_settings_from_dict = OwnedMediaProfileSettings.from_dict(owned_media_profile_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


