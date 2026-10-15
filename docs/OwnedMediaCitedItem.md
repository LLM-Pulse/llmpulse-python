# OwnedMediaCitedItem

The post, video, profile or channel. Null when nothing in the window matches it

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **str** | post covers posts and videos, profile covers profiles and channels | [optional] 
**title** | **str** |  | [optional] 
**subtitle** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**image_url** | **str** |  | [optional] 
**yours** | **bool** |  | [optional] 
**var_date** | **datetime** | Publication date of a post or video | [optional] 
**stats** | [**OwnedMediaCitedItemStats**](OwnedMediaCitedItemStats.md) |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_cited_item import OwnedMediaCitedItem

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaCitedItem from a JSON string
owned_media_cited_item_instance = OwnedMediaCitedItem.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaCitedItem.to_json())

# convert the object into a dict
owned_media_cited_item_dict = owned_media_cited_item_instance.to_dict()
# create an instance of OwnedMediaCitedItem from a dict
owned_media_cited_item_from_dict = OwnedMediaCitedItem.from_dict(owned_media_cited_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


