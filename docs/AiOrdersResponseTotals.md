# AiOrdersResponseTotals


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orders** | **int** |  | 
**revenue** | **str** | Decimal amount with two decimals, e.g. 1834.20 | 

## Example

```python
from llmpulse.models.ai_orders_response_totals import AiOrdersResponseTotals

# TODO update the JSON string below
json = "{}"
# create an instance of AiOrdersResponseTotals from a JSON string
ai_orders_response_totals_instance = AiOrdersResponseTotals.from_json(json)
# print the JSON string representation of the object
print(AiOrdersResponseTotals.to_json())

# convert the object into a dict
ai_orders_response_totals_dict = ai_orders_response_totals_instance.to_dict()
# create an instance of AiOrdersResponseTotals from a dict
ai_orders_response_totals_from_dict = AiOrdersResponseTotals.from_dict(ai_orders_response_totals_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


