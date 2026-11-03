# AiModelSentimentRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** | AI model key, as /dimensions/models lists it | [optional] 
**label** | **str** | Display name of the model | [optional] 
**color** | **str** | Hex color the app charts the model with | [optional] 
**sentiments_count** | **int** | Brand sentiment verdicts in the model&#39;s answers | [optional] 
**positive_count** | **int** | Positive and very positive verdicts | [optional] 
**negative_count** | **int** | Negative and very negative verdicts | [optional] 
**net_sentiment** | **float** | positive_count minus negative_count as a percentage (-100 to 100) of sentiments_count, neutral verdicts counted in the base; null when sentiments_count is 0 | [optional] 

## Example

```python
from llmpulse.models.ai_model_sentiment_row import AiModelSentimentRow

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelSentimentRow from a JSON string
ai_model_sentiment_row_instance = AiModelSentimentRow.from_json(json)
# print the JSON string representation of the object
print(AiModelSentimentRow.to_json())

# convert the object into a dict
ai_model_sentiment_row_dict = ai_model_sentiment_row_instance.to_dict()
# create an instance of AiModelSentimentRow from a dict
ai_model_sentiment_row_from_dict = AiModelSentimentRow.from_dict(ai_model_sentiment_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


