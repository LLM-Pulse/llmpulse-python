# OwnedMediaCitedItemStats

The counts the platform reports for the item; absent keys are unknown

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**citations** | **int** |  | [optional] 
**likes** | **int** |  | [optional] 
**comments** | **int** |  | [optional] 
**views** | **int** |  | [optional] 
**followers** | **int** |  | [optional] 
**unique_posts** | **int** |  | [optional] 
**unique_videos** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_cited_item_stats import OwnedMediaCitedItemStats

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaCitedItemStats from a JSON string
owned_media_cited_item_stats_instance = OwnedMediaCitedItemStats.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaCitedItemStats.to_json())

# convert the object into a dict
owned_media_cited_item_stats_dict = owned_media_cited_item_stats_instance.to_dict()
# create an instance of OwnedMediaCitedItemStats from a dict
owned_media_cited_item_stats_from_dict = OwnedMediaCitedItemStats.from_dict(owned_media_cited_item_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


