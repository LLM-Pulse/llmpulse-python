# UpdateOwnedMediaProfilesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**youtube_channel_url** | **str** | The main YouTube channel URL (@handle, /channel/UC..., /c/... or /user/...). An empty string or null clears it | [optional] 
**app_store_url** | **str** | The App Store app URL, with its id number. An empty string or null clears it | [optional] 
**google_play_url** | **str** | The Google Play app URL, or its package name (com.acme.app). An empty string or null clears it | [optional] 
**instagram_profile_url** | **str** | The main Instagram profile URL. An empty string or null clears it | [optional] 
**facebook_page_url** | **str** | The main Facebook Page URL. An empty string or null clears it | [optional] 
**tiktok_profile_url** | **str** | The main TikTok profile URL. An empty string or null clears it | [optional] 
**linkedin_company_url** | **str** | The main LinkedIn page URL: a company (/company/...), school (/school/...) or showcase (/showcase/...) page. An empty string or null clears it | [optional] 
**youtube_extra_profile_urls** | **List[str]** | FULL replacement list of extra YouTube channel URLs (at most 10); [] clears it | [optional] 
**mobile_apps_extra_profile_urls** | **List[str]** | FULL replacement list of extra App Store or Google Play app URLs (at most 10); [] clears it | [optional] 
**instagram_extra_profile_urls** | **List[str]** | FULL replacement list of extra Instagram profile URLs (at most 10); [] clears it | [optional] 
**facebook_extra_profile_urls** | **List[str]** | FULL replacement list of extra Facebook Page URLs (at most 10); [] clears it | [optional] 
**tiktok_extra_profile_urls** | **List[str]** | FULL replacement list of extra TikTok profile URLs (at most 10); [] clears it | [optional] 
**linkedin_extra_profile_urls** | **List[str]** | FULL replacement list of extra LinkedIn company, school or showcase page URLs (at most 10); [] clears it | [optional] 
**reddit_subreddits** | **List[str]** | FULL replacement list (at most 10) of subreddit names the brand owns, without r/; [] clears it | [optional] 
**reddit_usernames** | **List[str]** | FULL replacement list (at most 25) of Reddit usernames the brand owns, without u/; [] clears it | [optional] 

## Example

```python
from llmpulse.models.update_owned_media_profiles_request import UpdateOwnedMediaProfilesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateOwnedMediaProfilesRequest from a JSON string
update_owned_media_profiles_request_instance = UpdateOwnedMediaProfilesRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateOwnedMediaProfilesRequest.to_json())

# convert the object into a dict
update_owned_media_profiles_request_dict = update_owned_media_profiles_request_instance.to_dict()
# create an instance of UpdateOwnedMediaProfilesRequest from a dict
update_owned_media_profiles_request_from_dict = UpdateOwnedMediaProfilesRequest.from_dict(update_owned_media_profiles_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


