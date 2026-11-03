# AiModelSentimentCell


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | The actor&#39;s net sentiment in the model, positive_count minus negative_count as a percentage (-100 to 100) of total_sentiments; null when total_sentiments is 0 | [optional] 
**total_sentiments** | **int** | The actor&#39;s sentiment verdicts in the model&#39;s answers | [optional] 
**positive_count** | **int** | Positive and very positive verdicts | [optional] 
**negative_count** | **int** | Negative and very negative verdicts | [optional] 

## Example

```python
from llmpulse.models.ai_model_sentiment_cell import AiModelSentimentCell

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelSentimentCell from a JSON string
ai_model_sentiment_cell_instance = AiModelSentimentCell.from_json(json)
# print the JSON string representation of the object
print(AiModelSentimentCell.to_json())

# convert the object into a dict
ai_model_sentiment_cell_dict = ai_model_sentiment_cell_instance.to_dict()
# create an instance of AiModelSentimentCell from a dict
ai_model_sentiment_cell_from_dict = AiModelSentimentCell.from_dict(ai_model_sentiment_cell_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


