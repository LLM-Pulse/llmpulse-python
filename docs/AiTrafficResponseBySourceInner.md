# AiTrafficResponseBySourceInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | **str** | AI source slug, such as chatgpt or perplexity | 
**name** | **str** | Display name of the source | 
**users** | **int** |  | 
**sessions** | **int** |  | 
**conversions** | **int** |  | 

## Example

```python
from llmpulse.models.ai_traffic_response_by_source_inner import AiTrafficResponseBySourceInner

# TODO update the JSON string below
json = "{}"
# create an instance of AiTrafficResponseBySourceInner from a JSON string
ai_traffic_response_by_source_inner_instance = AiTrafficResponseBySourceInner.from_json(json)
# print the JSON string representation of the object
print(AiTrafficResponseBySourceInner.to_json())

# convert the object into a dict
ai_traffic_response_by_source_inner_dict = ai_traffic_response_by_source_inner_instance.to_dict()
# create an instance of AiTrafficResponseBySourceInner from a dict
ai_traffic_response_by_source_inner_from_dict = AiTrafficResponseBySourceInner.from_dict(ai_traffic_response_by_source_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


