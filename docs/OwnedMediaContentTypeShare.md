# OwnedMediaContentTypeShare


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content_type** | **str** | reel, post or tv on Instagram, post or pulse on LinkedIn, regular, shorts or live on YouTube | [optional] 
**citations** | **int** |  | [optional] 
**share_pct** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_content_type_share import OwnedMediaContentTypeShare

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaContentTypeShare from a JSON string
owned_media_content_type_share_instance = OwnedMediaContentTypeShare.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaContentTypeShare.to_json())

# convert the object into a dict
owned_media_content_type_share_dict = owned_media_content_type_share_instance.to_dict()
# create an instance of OwnedMediaContentTypeShare from a dict
owned_media_content_type_share_from_dict = OwnedMediaContentTypeShare.from_dict(owned_media_content_type_share_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


