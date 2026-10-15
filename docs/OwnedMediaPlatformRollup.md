# OwnedMediaPlatformRollup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** |  | [optional] 
**connected** | **bool** |  | [optional] 
**total** | **int** |  | [optional] 
**yours** | **int** |  | [optional] 
**share_pct** | **float** |  | [optional] 
**weekly** | [**List[OwnedMediaPlatformRollupWeeklyInner]**](OwnedMediaPlatformRollupWeeklyInner.md) |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_platform_rollup import OwnedMediaPlatformRollup

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaPlatformRollup from a JSON string
owned_media_platform_rollup_instance = OwnedMediaPlatformRollup.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaPlatformRollup.to_json())

# convert the object into a dict
owned_media_platform_rollup_dict = owned_media_platform_rollup_instance.to_dict()
# create an instance of OwnedMediaPlatformRollup from a dict
owned_media_platform_rollup_from_dict = OwnedMediaPlatformRollup.from_dict(owned_media_platform_rollup_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


