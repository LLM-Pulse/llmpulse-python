# OwnedMediaRow

One row of /dimensions/owned_media. Fields depend on provider and view: videos (title, url, channel_name, channel_handle, channel_url, video_id, thumbnail_url, views, published_at), channels (key, name, handle, url, avatar_url, unique_videos), posts (url, caption, owner_handle, thumbnail_url, content_type, likes, comments, views, posted_at), profiles (handle, name, url, avatar_url, followers, unique_posts), own_citations (url, citation_date, position, model), apps (domain, total_responses, rank, global_rank), the Trustpilot views profiles (key, name, rating, reviews_count, url, competitor_id), brands (name, domain, key, rating, rating_change, reviews_count, status, url, competitor_id) and reviews (id, brand, rating, title, text, author, published_at, replied, url, competitor_id), and activity (date, entity_id, entity_name, entity_url, yours, citations, plus store and competitor_id where applicable). Activity rows identify a reporting-period start; entity metadata is optional, and entity_id, entity_name and entity_url can be null when unknown. Store and competitor_id appear only where applicable. Every view but own_citations carries citations and yours; videos, channels, posts and profiles carry avg_position.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | The start date of the actual reporting period (view&#x3D;activity) | [optional] 
**entity_id** | **str** | Platform entity identifier (view&#x3D;activity) | [optional] 
**entity_name** | **str** | Current entity name when known (view&#x3D;activity) | [optional] 
**entity_url** | **str** | Current profile, channel or app listing URL when known (view&#x3D;activity) | [optional] 
**store** | **str** | Store selected for provider&#x3D;mobile_apps (view&#x3D;activity) | [optional] 
**competitor_id** | **int** | Competitor identifier when the row represents a competitor&#39;s app or Trustpilot profile | [optional] 
**id** | **int** | The review&#39;s identifier (provider&#x3D;trustpilot, view&#x3D;reviews) | [optional] 
**brand** | **str** | The brand or competitor whose Trustpilot profile carries the review (provider&#x3D;trustpilot, view&#x3D;reviews) | [optional] 
**rating** | **float** | Trustpilot rating out of 5: the profile&#39;s at its last monthly read (views profiles and brands) or the review&#39;s stars (view&#x3D;reviews) | [optional] 
**rating_change** | **float** | Change of the profile&#39;s rating since the previous monthly read (provider&#x3D;trustpilot, view&#x3D;brands); null before a second read | [optional] 
**reviews_count** | **int** | The profile&#39;s review count on Trustpilot at its last monthly read (provider&#x3D;trustpilot) | [optional] 
**status** | **str** | Whether the brand&#39;s Trustpilot profile has been read (found), Trustpilot has no business for its domain (not_found), or it has not been read yet (pending) (provider&#x3D;trustpilot, view&#x3D;brands) | [optional] 
**text** | **str** | The review text (provider&#x3D;trustpilot, view&#x3D;reviews) | [optional] 
**author** | **str** | The reviewer&#39;s display name (provider&#x3D;trustpilot, view&#x3D;reviews) | [optional] 
**replied** | **bool** | Whether the business replied to the review (provider&#x3D;trustpilot, view&#x3D;reviews) | [optional] 
**title** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**channel_name** | **str** |  | [optional] 
**channel_handle** | **str** | The video&#39;s channel handle, without the @ | [optional] 
**channel_url** | **str** |  | [optional] 
**video_id** | **str** |  | [optional] 
**key** | **str** | The channel key (handle:..., channel:... or name:...), accepted as profile by /dimensions/owned_media/citing_prompts; on provider&#x3D;trustpilot, the business domain the profile is filed under, null for a brand without a domain | [optional] 
**name** | **str** |  | [optional] 
**handle** | **str** |  | [optional] 
**caption** | **str** |  | [optional] 
**owner_handle** | **str** |  | [optional] 
**thumbnail_url** | **str** | The post or video image. Our cached copy where one exists, so the link does not expire | [optional] 
**avatar_url** | **str** | The profile or channel image. Our cached copy where one exists | [optional] 
**content_type** | **str** | The post format on its platform: reel, post or tv on Instagram, post or pulse on LinkedIn, post elsewhere | [optional] 
**citations** | **int** | Citations for the row; for view&#x3D;activity, the count in this reporting period | [optional] 
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
**domain** | **str** | The app&#39;s store listing URL (provider&#x3D;mobile_apps), or the brand&#39;s domain (provider&#x3D;trustpilot, view&#x3D;brands) | [optional] 
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


