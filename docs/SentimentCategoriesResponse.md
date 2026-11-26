# SentimentCategoriesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**sentiments** | [**List[SentimentCategory]**](SentimentCategory.md) |  | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.sentiment_categories_response import SentimentCategoriesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentCategoriesResponse from a JSON string
sentiment_categories_response_instance = SentimentCategoriesResponse.from_json(json)
# print the JSON string representation of the object
print(SentimentCategoriesResponse.to_json())

# convert the object into a dict
sentiment_categories_response_dict = sentiment_categories_response_instance.to_dict()
# create an instance of SentimentCategoriesResponse from a dict
sentiment_categories_response_from_dict = SentimentCategoriesResponse.from_dict(sentiment_categories_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


