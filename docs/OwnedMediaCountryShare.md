# OwnedMediaCountryShare


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country_code** | **str** |  | [optional] 
**citations** | **int** |  | [optional] 
**share_pct** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_country_share import OwnedMediaCountryShare

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaCountryShare from a JSON string
owned_media_country_share_instance = OwnedMediaCountryShare.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaCountryShare.to_json())

# convert the object into a dict
owned_media_country_share_dict = owned_media_country_share_instance.to_dict()
# create an instance of OwnedMediaCountryShare from a dict
owned_media_country_share_from_dict = OwnedMediaCountryShare.from_dict(owned_media_country_share_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


