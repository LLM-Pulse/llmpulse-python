# SentimentCategory


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **str** | The metric key of the level (sentiment_&lt;key&gt;) | 
**key** | **str** | very_positive, positive, neutral, negative or very_negative | 
**label** | **str** |  | 
**color** | **str** | Hex color the app shows the level in | 
**score** | **float** | Score of the level, from -1.0 (very_negative) to 1.0 (very_positive) | 

## Example

```python
from llmpulse.models.sentiment_category import SentimentCategory

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentCategory from a JSON string
sentiment_category_instance = SentimentCategory.from_json(json)
# print the JSON string representation of the object
print(SentimentCategory.to_json())

# convert the object into a dict
sentiment_category_dict = sentiment_category_instance.to_dict()
# create an instance of SentimentCategory from a dict
sentiment_category_from_dict = SentimentCategory.from_dict(sentiment_category_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


