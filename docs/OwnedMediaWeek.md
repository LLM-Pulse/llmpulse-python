# OwnedMediaWeek


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**week** | **date** | The Monday that starts the week | [optional] 
**citations** | **int** |  | [optional] 
**yours** | **int** | Null for provider&#x3D;overview, whose rollups have no weekly split | [optional] 
**other** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_week import OwnedMediaWeek

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaWeek from a JSON string
owned_media_week_instance = OwnedMediaWeek.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaWeek.to_json())

# convert the object into a dict
owned_media_week_dict = owned_media_week_instance.to_dict()
# create an instance of OwnedMediaWeek from a dict
owned_media_week_from_dict = OwnedMediaWeek.from_dict(owned_media_week_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


