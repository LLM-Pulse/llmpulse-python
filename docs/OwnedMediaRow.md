# OwnedMediaRow

One row of /dimensions/owned_media. Fields depend on provider and view: videos (title, url, channel_name, channel_handle, channel_url, video_id, thumbnail_url, views, published_at), channels (key, name, handle, url, avatar_url, unique_videos), posts (url, caption, owner_handle, thumbnail_url, content_type, likes, comments, views, posted_at), profiles (handle, name, url, avatar_url, followers, unique_posts), own_citations (url, citation_date, position, model) and apps (domain, total_responses, rank, global_rank). Every view but own_citations carries citations and yours; videos, channels, posts and profiles carry avg_position.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**channel_name** | **str** |  | [optional] 
**channel_handle** | **str** | The video&#39;s channel handle, without the @ | [optional] 
**channel_url** | **str** |  | [optional] 
**video_id** | **str** |  | [optional] 
**key** | **str** | The channel key (handle:..., channel:... or name:...), accepted as profile by /dimensions/owned_media/citing_prompts | [optional] 
**name** | **str** |  | [optional] 
**handle** | **str** |  | [optional] 
**caption** | **str** |  | [optional] 
**owner_handle** | **str** |  | [optional] 
**thumbnail_url** | **str** | The post or video image. Our cached copy where one exists, so the link does not expire | [optional] 
**avatar_url** | **str** | The profile or channel image. Our cached copy where one exists | [optional] 
**content_type** | **str** | The post format on its platform: reel, post or tv on Instagram, post or pulse on LinkedIn, post elsewhere | [optional] 
**citations** | **int** |  | [optional] 
**unique_videos** | **int** |  | [optional] 
**unique_posts** | **int** |  | [optional] 
**followers** | **int** |  | [optional] 
**likes** | **int** |  | [optional] 
**comments** | **int** |  | [optional] 
**views** | **object** | View count as the platform reports it, a number or a numeric string, or null when unknown | [optional] 
**published_at** | **str** | Publication date as the platform reports it | [optional] 
**posted_at** | **str** | Publication date as the platform reports it (ISO 8601, or Unix seconds on TikTok) | [optional] 
**avg_position** | **float** | Average position of the citation in the answers (1 &#x3D; first); null when unknown | [optional] 
**yours** | **bool** |  | [optional] 
**citation_date** | **datetime** |  | [optional] 
**position** | **int** |  | [optional] 
**model** | **str** |  | [optional] 
**domain** | **str** | The app&#39;s store listing URL (provider&#x3D;mobile_apps) | [optional] 
**total_responses** | **int** |  | [optional] 
**rank** | **int** |  | [optional] 
**global_rank** | **int** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_row import OwnedMediaRow

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaRow from a JSON string
owned_media_row_instance = OwnedMediaRow.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaRow.to_json())

# convert the object into a dict
owned_media_row_dict = owned_media_row_instance.to_dict()
# create an instance of OwnedMediaRow from a dict
owned_media_row_from_dict = OwnedMediaRow.from_dict(owned_media_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


