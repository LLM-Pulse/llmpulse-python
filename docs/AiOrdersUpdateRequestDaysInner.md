# AiOrdersUpdateRequestDaysInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**day** | **date** | Must fall inside from..to | 
**referrer** | **str** | Raw referring host or utm_source of the order&#39;s first visit, e.g. chatgpt.com. Entries that are not an AI assistant are ignored | 
**orders** | **int** |  | 
**revenue** | **str** | Non-negative decimal amount in currency, e.g. 120.50. A JSON number is accepted too | 

## Example

```python
from llmpulse.models.ai_orders_update_request_days_inner import AiOrdersUpdateRequestDaysInner

# TODO update the JSON string below
json = "{}"
# create an instance of AiOrdersUpdateRequestDaysInner from a JSON string
ai_orders_update_request_days_inner_instance = AiOrdersUpdateRequestDaysInner.from_json(json)
# print the JSON string representation of the object
print(AiOrdersUpdateRequestDaysInner.to_json())

# convert the object into a dict
ai_orders_update_request_days_inner_dict = ai_orders_update_request_days_inner_instance.to_dict()
# create an instance of AiOrdersUpdateRequestDaysInner from a dict
ai_orders_update_request_days_inner_from_dict = AiOrdersUpdateRequestDaysInner.from_dict(ai_orders_update_request_days_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


