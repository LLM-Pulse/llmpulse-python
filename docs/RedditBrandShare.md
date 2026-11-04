# RedditBrandShare


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actor_id** | **int** |  | 
**actor_name** | **str** |  | 
**is_brand** | **bool** |  | 
**citations** | **int** |  | 
**share_pct** | **float** | Percentage (0-100) among the tracked brand and competitors with cited mentions | 

## Example

```python
from llmpulse.models.reddit_brand_share import RedditBrandShare

# TODO update the JSON string below
json = "{}"
# create an instance of RedditBrandShare from a JSON string
reddit_brand_share_instance = RedditBrandShare.from_json(json)
# print the JSON string representation of the object
print(RedditBrandShare.to_json())

# convert the object into a dict
reddit_brand_share_dict = reddit_brand_share_instance.to_dict()
# create an instance of RedditBrandShare from a dict
reddit_brand_share_from_dict = RedditBrandShare.from_dict(reddit_brand_share_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


