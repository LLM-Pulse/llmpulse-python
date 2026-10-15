# OwnedMediaModelShare


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** |  | [optional] 
**citations** | **int** |  | [optional] 
**share_pct** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_model_share import OwnedMediaModelShare

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaModelShare from a JSON string
owned_media_model_share_instance = OwnedMediaModelShare.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaModelShare.to_json())

# convert the object into a dict
owned_media_model_share_dict = owned_media_model_share_instance.to_dict()
# create an instance of OwnedMediaModelShare from a dict
owned_media_model_share_from_dict = OwnedMediaModelShare.from_dict(owned_media_model_share_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


