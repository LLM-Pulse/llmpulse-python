# AiOrdersUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**platform** | **str** |  | 
**currency** | **str** | ISO 4217 code, e.g. EUR | 
**var_from** | **date** | First day of the window this push replaces | 
**to** | **date** | Last day of the window; at most 400 days after from | 
**days** | [**List[AiOrdersUpdateRequestDaysInner]**](AiOrdersUpdateRequestDaysInner.md) |  | 

## Example

```python
from llmpulse.models.ai_orders_update_request import AiOrdersUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AiOrdersUpdateRequest from a JSON string
ai_orders_update_request_instance = AiOrdersUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(AiOrdersUpdateRequest.to_json())

# convert the object into a dict
ai_orders_update_request_dict = ai_orders_update_request_instance.to_dict()
# create an instance of AiOrdersUpdateRequest from a dict
ai_orders_update_request_from_dict = AiOrdersUpdateRequest.from_dict(ai_orders_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


