# RedditSubredditActivityPeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | Start date of the actual reporting period | 
**subreddit** | **str** | Subreddit name, or null for the Others aggregate | 
**is_others** | **bool** |  | 
**citations** | **int** |  | 

## Example

```python
from llmpulse.models.reddit_subreddit_activity_period import RedditSubredditActivityPeriod

# TODO update the JSON string below
json = "{}"
# create an instance of RedditSubredditActivityPeriod from a JSON string
reddit_subreddit_activity_period_instance = RedditSubredditActivityPeriod.from_json(json)
# print the JSON string representation of the object
print(RedditSubredditActivityPeriod.to_json())

# convert the object into a dict
reddit_subreddit_activity_period_dict = reddit_subreddit_activity_period_instance.to_dict()
# create an instance of RedditSubredditActivityPeriod from a dict
reddit_subreddit_activity_period_from_dict = RedditSubredditActivityPeriod.from_dict(reddit_subreddit_activity_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


