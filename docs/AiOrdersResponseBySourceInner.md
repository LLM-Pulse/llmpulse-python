# AiOrdersResponseBySourceInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | **str** | AI assistant slug, e.g. chatgpt or perplexity | 
**name** | **str** | Display name, e.g. ChatGPT | 
**orders** | **int** |  | 
**revenue** | **str** |  | 

## Example

```python
from llmpulse.models.ai_orders_response_by_source_inner import AiOrdersResponseBySourceInner

# TODO update the JSON string below
json = "{}"
# create an instance of AiOrdersResponseBySourceInner from a JSON string
ai_orders_response_by_source_inner_instance = AiOrdersResponseBySourceInner.from_json(json)
# print the JSON string representation of the object
print(AiOrdersResponseBySourceInner.to_json())

# convert the object into a dict
ai_orders_response_by_source_inner_dict = ai_orders_response_by_source_inner_instance.to_dict()
# create an instance of AiOrdersResponseBySourceInner from a dict
ai_orders_response_by_source_inner_from_dict = AiOrdersResponseBySourceInner.from_dict(ai_orders_response_by_source_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


