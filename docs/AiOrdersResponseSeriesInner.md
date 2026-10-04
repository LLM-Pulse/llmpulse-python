# AiOrdersResponseSeriesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**day** | **date** |  | 
**orders** | **int** |  | 
**revenue** | **str** |  | 

## Example

```python
from llmpulse.models.ai_orders_response_series_inner import AiOrdersResponseSeriesInner

# TODO update the JSON string below
json = "{}"
# create an instance of AiOrdersResponseSeriesInner from a JSON string
ai_orders_response_series_inner_instance = AiOrdersResponseSeriesInner.from_json(json)
# print the JSON string representation of the object
print(AiOrdersResponseSeriesInner.to_json())

# convert the object into a dict
ai_orders_response_series_inner_dict = ai_orders_response_series_inner_instance.to_dict()
# create an instance of AiOrdersResponseSeriesInner from a dict
ai_orders_response_series_inner_from_dict = AiOrdersResponseSeriesInner.from_dict(ai_orders_response_series_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


