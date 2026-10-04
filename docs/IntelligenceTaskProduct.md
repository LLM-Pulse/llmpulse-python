# IntelligenceTaskProduct

The store product a product_listing task rewrites

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**external_id** | **str** |  | [optional] 
**title** | **str** |  | 
**description_html** | **str** |  | [optional] 
**seo_title** | **str** |  | [optional] 
**seo_description** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**product_type** | **str** |  | [optional] 
**images** | [**List[IntelligenceTaskProductImagesInner]**](IntelligenceTaskProductImagesInner.md) |  | [optional] 

## Example

```python
from llmpulse.models.intelligence_task_product import IntelligenceTaskProduct

# TODO update the JSON string below
json = "{}"
# create an instance of IntelligenceTaskProduct from a JSON string
intelligence_task_product_instance = IntelligenceTaskProduct.from_json(json)
# print the JSON string representation of the object
print(IntelligenceTaskProduct.to_json())

# convert the object into a dict
intelligence_task_product_dict = intelligence_task_product_instance.to_dict()
# create an instance of IntelligenceTaskProduct from a dict
intelligence_task_product_from_dict = IntelligenceTaskProduct.from_dict(intelligence_task_product_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


