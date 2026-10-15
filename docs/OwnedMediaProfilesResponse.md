# OwnedMediaProfilesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**platforms** | [**List[OwnedMediaPlatformProfiles]**](OwnedMediaPlatformProfiles.md) |  | [optional] 
**settings** | [**OwnedMediaProfileSettings**](OwnedMediaProfileSettings.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_profiles_response import OwnedMediaProfilesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaProfilesResponse from a JSON string
owned_media_profiles_response_instance = OwnedMediaProfilesResponse.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaProfilesResponse.to_json())

# convert the object into a dict
owned_media_profiles_response_dict = owned_media_profiles_response_instance.to_dict()
# create an instance of OwnedMediaProfilesResponse from a dict
owned_media_profiles_response_from_dict = OwnedMediaProfilesResponse.from_dict(owned_media_profiles_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


