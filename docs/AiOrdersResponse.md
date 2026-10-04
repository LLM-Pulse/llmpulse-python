# AiOrdersResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**platform** | **str** |  | 
**currency** | **str** | ISO 4217 code of the most recent stored day; null when the window holds no stored order | 
**var_from** | **date** |  | 
**to** | **date** |  | 
**totals** | [**AiOrdersResponseTotals**](AiOrdersResponseTotals.md) |  | 
**by_source** | [**List[AiOrdersResponseBySourceInner]**](AiOrdersResponseBySourceInner.md) | One row per AI assistant, highest revenue first | 
**series** | [**List[AiOrdersResponseSeriesInner]**](AiOrdersResponseSeriesInner.md) | Days that have stored orders, oldest first | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.ai_orders_response import AiOrdersResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AiOrdersResponse from a JSON string
ai_orders_response_instance = AiOrdersResponse.from_json(json)
# print the JSON string representation of the object
print(AiOrdersResponse.to_json())

# convert the object into a dict
ai_orders_response_dict = ai_orders_response_instance.to_dict()
# create an instance of AiOrdersResponse from a dict
ai_orders_response_from_dict = AiOrdersResponse.from_dict(ai_orders_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


