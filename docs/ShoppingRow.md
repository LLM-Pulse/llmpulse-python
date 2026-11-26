# ShoppingRow

One row of /dimensions/shopping. Fields depend on view: products (product_key, title, domain, url, merchants, currency, currency_count, min_price, max_price, avg_rating, rating_votes, appearances, is_client, best_rank, models, last_seen_at) and merchants (merchant, appearances, products, currency, min_price, max_price, avg_price, avg_rating).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**product_key** | **str** | Stable grouping key of the product: its external id, else title: and the lowercased title (view&#x3D;products) | [optional] 
**title** | **str** |  | [optional] 
**domain** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**merchants** | **str** | The merchants the product card names (view&#x3D;products) | [optional] 
**merchant** | **str** | The merchant (view&#x3D;merchants) | [optional] 
**products** | **int** | Distinct products the merchant sold (view&#x3D;merchants) | [optional] 
**currency** | **str** | Currency code the prices are in; null when no price names one | 
**currency_count** | **int** | Currencies the product was priced in; above 1 the row reports its highest-priced listing (view&#x3D;products) | [optional] 
**min_price** | **float** |  | 
**max_price** | **float** |  | 
**avg_price** | **float** | Average price in currency (view&#x3D;merchants) | [optional] 
**avg_rating** | **float** |  | 
**rating_votes** | **int** | Most rating votes any listing of the product showed (view&#x3D;products) | [optional] 
**appearances** | **int** |  | 
**is_client** | **bool** | Whether the product is identified as your brand&#39;s own (view&#x3D;products) | [optional] 
**best_rank** | **int** | Best rank the product got in a card list (view&#x3D;products) | [optional] 
**models** | **List[str]** | Models that showed the product (view&#x3D;products) | [optional] 
**last_seen_at** | **datetime** | The latest answer that showed the product (view&#x3D;products) | [optional] 

## Example

```python
from llmpulse.models.shopping_row import ShoppingRow

# TODO update the JSON string below
json = "{}"
# create an instance of ShoppingRow from a JSON string
shopping_row_instance = ShoppingRow.from_json(json)
# print the JSON string representation of the object
print(ShoppingRow.to_json())

# convert the object into a dict
shopping_row_dict = shopping_row_instance.to_dict()
# create an instance of ShoppingRow from a dict
shopping_row_from_dict = ShoppingRow.from_dict(shopping_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


