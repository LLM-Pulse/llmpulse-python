# OwnedMediaAgeBucketShare


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bucket** | **str** | Age of the cited post or video when the summary is read | [optional] 
**citations** | **int** |  | [optional] 
**share_pct** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_age_bucket_share import OwnedMediaAgeBucketShare

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaAgeBucketShare from a JSON string
owned_media_age_bucket_share_instance = OwnedMediaAgeBucketShare.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaAgeBucketShare.to_json())

# convert the object into a dict
owned_media_age_bucket_share_dict = owned_media_age_bucket_share_instance.to_dict()
# create an instance of OwnedMediaAgeBucketShare from a dict
owned_media_age_bucket_share_from_dict = OwnedMediaAgeBucketShare.from_dict(owned_media_age_bucket_share_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


