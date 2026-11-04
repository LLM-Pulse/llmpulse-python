# OwnedMediaPlatformActivityPeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | Start date of the actual reporting period | 
**citations** | **int** |  | 

## Example

```python
from llmpulse.models.owned_media_platform_activity_period import OwnedMediaPlatformActivityPeriod

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaPlatformActivityPeriod from a JSON string
owned_media_platform_activity_period_instance = OwnedMediaPlatformActivityPeriod.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaPlatformActivityPeriod.to_json())

# convert the object into a dict
owned_media_platform_activity_period_dict = owned_media_platform_activity_period_instance.to_dict()
# create an instance of OwnedMediaPlatformActivityPeriod from a dict
owned_media_platform_activity_period_from_dict = OwnedMediaPlatformActivityPeriod.from_dict(owned_media_platform_activity_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


