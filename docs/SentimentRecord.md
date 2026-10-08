# SentimentRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**prompt_execution_id** | **int** |  | 
**prompt_text** | **str** |  | 
**model** | **str** |  | 
**analysis** | **str** |  | 
**score** | **float** | From -1 (very negative) to 1 (very positive) | 
**comment** | **str** |  | 
**topics** | **str** | Comma-separated topics | 
**competitor_id** | **int** | Null for a sentiment about the project&#39;s own brand | 
**competitor_name** | **str** | Null for a sentiment about the project&#39;s own brand | 
**is_brand_sentiment** | **bool** |  | 
**executed_at** | **datetime** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.sentiment_record import SentimentRecord

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentRecord from a JSON string
sentiment_record_instance = SentimentRecord.from_json(json)
# print the JSON string representation of the object
print(SentimentRecord.to_json())

# convert the object into a dict
sentiment_record_dict = sentiment_record_instance.to_dict()
# create an instance of SentimentRecord from a dict
sentiment_record_from_dict = SentimentRecord.from_dict(sentiment_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


