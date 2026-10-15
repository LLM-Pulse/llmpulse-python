# SentimentBreakdownEnvelope


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_from** | **datetime** |  | 
**to** | **datetime** |  | 
**brand** | [**SentimentBreakdownBrand**](SentimentBreakdownBrand.md) |  | 
**sort** | **str** |  | 
**sort_dir** | **str** |  | 

## Example

```python
from llmpulse.models.sentiment_breakdown_envelope import SentimentBreakdownEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of SentimentBreakdownEnvelope from a JSON string
sentiment_breakdown_envelope_instance = SentimentBreakdownEnvelope.from_json(json)
# print the JSON string representation of the object
print(SentimentBreakdownEnvelope.to_json())

# convert the object into a dict
sentiment_breakdown_envelope_dict = sentiment_breakdown_envelope_instance.to_dict()
# create an instance of SentimentBreakdownEnvelope from a dict
sentiment_breakdown_envelope_from_dict = SentimentBreakdownEnvelope.from_dict(sentiment_breakdown_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


