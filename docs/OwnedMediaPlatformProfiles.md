# OwnedMediaPlatformProfiles


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **str** |  | [optional] 
**connected** | **bool** |  | [optional] 
**max_extra_profiles** | **int** | How many extra profiles the platform accepts; null where it takes none | [optional] 
**profiles** | [**List[OwnedMediaProfile]**](OwnedMediaProfile.md) |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_platform_profiles import OwnedMediaPlatformProfiles

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaPlatformProfiles from a JSON string
owned_media_platform_profiles_instance = OwnedMediaPlatformProfiles.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaPlatformProfiles.to_json())

# convert the object into a dict
owned_media_platform_profiles_dict = owned_media_platform_profiles_instance.to_dict()
# create an instance of OwnedMediaPlatformProfiles from a dict
owned_media_platform_profiles_from_dict = OwnedMediaPlatformProfiles.from_dict(owned_media_platform_profiles_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


