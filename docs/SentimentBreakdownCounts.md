# SentimentBreakdownCounts


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

## Example

```python
from llmpulse.models.sentiment_breakdown_counts import SentimentBreakdownCounts

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentBreakdownCounts from a JSON string
sentiment_breakdown_counts_instance = SentimentBreakdownCounts.from_json(json)
# print the JSON string representation of the object
print(SentimentBreakdownCounts.to_json())

# convert the object into a dict
sentiment_breakdown_counts_dict = sentiment_breakdown_counts_instance.to_dict()
# create an instance of SentimentBreakdownCounts from a dict
sentiment_breakdown_counts_from_dict = SentimentBreakdownCounts.from_dict(sentiment_breakdown_counts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


