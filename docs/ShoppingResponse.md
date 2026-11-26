# ShoppingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**view** | **str** | products or merchants | 
**totals** | [**ShoppingTotals**](ShoppingTotals.md) |  | 
**data** | [**List[ShoppingRow]**](ShoppingRow.md) |  | 

## Example

```python
from llmpulse.models.shopping_response import ShoppingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ShoppingResponse from a JSON string
shopping_response_instance = ShoppingResponse.from_json(json)
# print the JSON string representation of the object
print(ShoppingResponse.to_json())

# convert the object into a dict
shopping_response_dict = shopping_response_instance.to_dict()
# create an instance of ShoppingResponse from a dict
shopping_response_from_dict = ShoppingResponse.from_dict(shopping_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


