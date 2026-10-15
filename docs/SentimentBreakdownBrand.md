# SentimentBreakdownBrand


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**id** | **int** | The competitor id when type is competitor | [optional] 
**name** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.sentiment_breakdown_brand import SentimentBreakdownBrand

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentBreakdownBrand from a JSON string
sentiment_breakdown_brand_instance = SentimentBreakdownBrand.from_json(json)
# print the JSON string representation of the object
print(SentimentBreakdownBrand.to_json())

# convert the object into a dict
sentiment_breakdown_brand_dict = sentiment_breakdown_brand_instance.to_dict()
# create an instance of SentimentBreakdownBrand from a dict
sentiment_breakdown_brand_from_dict = SentimentBreakdownBrand.from_dict(sentiment_breakdown_brand_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


