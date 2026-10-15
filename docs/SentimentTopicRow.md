# SentimentTopicRow


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
**topic** | **str** |  | 

## Example

```python
from llmpulse.models.sentiment_topic_row import SentimentTopicRow

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentTopicRow from a JSON string
sentiment_topic_row_instance = SentimentTopicRow.from_json(json)
# print the JSON string representation of the object
print(SentimentTopicRow.to_json())

# convert the object into a dict
sentiment_topic_row_dict = sentiment_topic_row_instance.to_dict()
# create an instance of SentimentTopicRow from a dict
sentiment_topic_row_from_dict = SentimentTopicRow.from_dict(sentiment_topic_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


