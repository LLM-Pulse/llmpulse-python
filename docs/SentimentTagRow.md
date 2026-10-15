# SentimentTagRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mentions** | **int** | Analyzed mentions | 
**positive** | **int** | Positive and very positive | 
**neutral** | **int** |  | 
**negative** | **int** | Negative and very negative | 
**positive_pct** | **float** |  | 
**neutral_pct** | **float** |  | 
**negative_pct** | **float** |  | 
**net_score** | **float** | Positive minus negative, divided by mentions, times 100 | 
**tag_id** | **int** |  | 
**tag** | **str** |  | 

## Example

```python
from llmpulse.models.sentiment_tag_row import SentimentTagRow

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentTagRow from a JSON string
sentiment_tag_row_instance = SentimentTagRow.from_json(json)
# print the JSON string representation of the object
print(SentimentTagRow.to_json())

# convert the object into a dict
sentiment_tag_row_dict = sentiment_tag_row_instance.to_dict()
# create an instance of SentimentTagRow from a dict
sentiment_tag_row_from_dict = SentimentTagRow.from_dict(sentiment_tag_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


