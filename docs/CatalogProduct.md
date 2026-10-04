# CatalogProduct


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**external_id** | **str** | The store&#39;s product id, e.g. gid://shopify/Product/1 | 
**title** | **str** |  | 
**handle** | **str** |  | [optional] 
**product_type** | **str** |  | [optional] 
**vendor** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**collections** | **List[str]** |  | [optional] 
**url** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.catalog_product import CatalogProduct

# TODO update the JSON string below
json = "{}"
# create an instance of CatalogProduct from a JSON string
catalog_product_instance = CatalogProduct.from_json(json)
# print the JSON string representation of the object
print(CatalogProduct.to_json())

# convert the object into a dict
catalog_product_dict = catalog_product_instance.to_dict()
# create an instance of CatalogProduct from a dict
catalog_product_from_dict = CatalogProduct.from_dict(catalog_product_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


