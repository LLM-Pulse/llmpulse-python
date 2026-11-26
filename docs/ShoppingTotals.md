# ShoppingTotals


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**products** | **int** |  | 
**your_products** | **int** |  | 
**merchants** | **int** |  | 
**avg_price** | **float** | Average price in avg_price_currency | 
**avg_price_currency** | **str** | The currency most prices use | 
**avg_rating** | **float** |  | 
**executions_with_shopping** | **int** |  | 

## Example

```python
from llmpulse.models.shopping_totals import ShoppingTotals

# TODO update the JSON string below
json = "{}"
# create an instance of ShoppingTotals from a JSON string
shopping_totals_instance = ShoppingTotals.from_json(json)
# print the JSON string representation of the object
print(ShoppingTotals.to_json())

# convert the object into a dict
shopping_totals_dict = shopping_totals_instance.to_dict()
# create an instance of ShoppingTotals from a dict
shopping_totals_from_dict = ShoppingTotals.from_dict(shopping_totals_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


