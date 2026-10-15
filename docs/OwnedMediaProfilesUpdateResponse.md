# OwnedMediaProfilesUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**platforms** | [**List[OwnedMediaPlatformProfiles]**](OwnedMediaPlatformProfiles.md) |  | [optional] 
**settings** | [**OwnedMediaProfileSettings**](OwnedMediaProfileSettings.md) |  | [optional] 
**request_id** | **str** |  | [optional] 
**updated_fields** | **List[str]** | The fields this request set | [optional] 
**profile_scrapes_queued** | **List[str]** | Platforms whose new profile is being scraped in the background for its name and avatar | [optional] 

## Example

```python
from llmpulse.models.owned_media_profiles_update_response import OwnedMediaProfilesUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaProfilesUpdateResponse from a JSON string
owned_media_profiles_update_response_instance = OwnedMediaProfilesUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaProfilesUpdateResponse.to_json())

# convert the object into a dict
owned_media_profiles_update_response_dict = owned_media_profiles_update_response_instance.to_dict()
# create an instance of OwnedMediaProfilesUpdateResponse from a dict
owned_media_profiles_update_response_from_dict = OwnedMediaProfilesUpdateResponse.from_dict(owned_media_profiles_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


