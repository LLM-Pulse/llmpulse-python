# RedditPositionShare


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bucket** | **str** |  | 
**citations** | **int** |  | 
**share_pct** | **float** | Percentage (0-100) of citations in the included position buckets | 

## Example

```python
from llmpulse.models.reddit_position_share import RedditPositionShare

# TODO update the JSON string below
json = "{}"
# create an instance of RedditPositionShare from a JSON string
reddit_position_share_instance = RedditPositionShare.from_json(json)
# print the JSON string representation of the object
print(RedditPositionShare.to_json())

# convert the object into a dict
reddit_position_share_dict = reddit_position_share_instance.to_dict()
# create an instance of RedditPositionShare from a dict
reddit_position_share_from_dict = RedditPositionShare.from_dict(reddit_position_share_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


