# RedditResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**view** | **str** | subreddits, authors, threads or breakdowns | 
**var_from** | **datetime** | Start of the window, 30 days back by default | 
**to** | **datetime** |  | 
**citations** | **int** | Reddit citations after the filters (view&#x3D;breakdowns) | [optional] 
**data** | [**List[RedditRow]**](RedditRow.md) |  | 

## Example

```python
from llmpulse.models.reddit_response import RedditResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RedditResponse from a JSON string
reddit_response_instance = RedditResponse.from_json(json)
# print the JSON string representation of the object
print(RedditResponse.to_json())

# convert the object into a dict
reddit_response_dict = reddit_response_instance.to_dict()
# create an instance of RedditResponse from a dict
reddit_response_from_dict = RedditResponse.from_dict(reddit_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


