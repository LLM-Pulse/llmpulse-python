# SentimentTagsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**var_from** | **datetime** |  | 
**to** | **datetime** |  | 
**brand** | [**SentimentBreakdownBrand**](SentimentBreakdownBrand.md) |  | 
**sort** | **str** |  | 
**sort_dir** | **str** |  | 
**data** | [**List[SentimentTagRow]**](SentimentTagRow.md) |  | 

## Example

```python
from llmpulse.models.sentiment_tags_response import SentimentTagsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentTagsResponse from a JSON string
sentiment_tags_response_instance = SentimentTagsResponse.from_json(json)
# print the JSON string representation of the object
print(SentimentTagsResponse.to_json())

# convert the object into a dict
sentiment_tags_response_dict = sentiment_tags_response_instance.to_dict()
# create an instance of SentimentTagsResponse from a dict
sentiment_tags_response_from_dict = SentimentTagsResponse.from_dict(sentiment_tags_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


