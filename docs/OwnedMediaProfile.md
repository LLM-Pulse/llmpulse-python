# OwnedMediaProfile


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | [optional] 
**handle** | **str** | The handle, page id, store app id, subreddit or username | [optional] 
**kind** | **str** |  | [optional] 
**main** | **bool** | True for the main profile of its platform (or store), false for an extra one | [optional] 
**store** | **str** | google_play or app_store for an app; null elsewhere | [optional] 
**name** | **str** |  | [optional] 
**avatar_url** | **str** |  | [optional] 
**scrape_status** | **str** | State of the profile scrape that reads its name and avatar: pending, running, ready, failed or skipped; null when none has started or the platform has none | [optional] 

## Example

```python
from llmpulse.models.owned_media_profile import OwnedMediaProfile

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaProfile from a JSON string
owned_media_profile_instance = OwnedMediaProfile.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaProfile.to_json())

# convert the object into a dict
owned_media_profile_dict = owned_media_profile_instance.to_dict()
# create an instance of OwnedMediaProfile from a dict
owned_media_profile_from_dict = OwnedMediaProfile.from_dict(owned_media_profile_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


