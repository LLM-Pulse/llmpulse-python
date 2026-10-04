# AiOrdersUpdateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**platform** | **str** |  | 
**stored** | **int** | Rows stored, one per day and AI assistant | 
**ignored** | **int** | Entries whose referrer is not an AI assistant | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.ai_orders_update_response import AiOrdersUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AiOrdersUpdateResponse from a JSON string
ai_orders_update_response_instance = AiOrdersUpdateResponse.from_json(json)
# print the JSON string representation of the object
print(AiOrdersUpdateResponse.to_json())

# convert the object into a dict
ai_orders_update_response_dict = ai_orders_update_response_instance.to_dict()
# create an instance of AiOrdersUpdateResponse from a dict
ai_orders_update_response_from_dict = AiOrdersUpdateResponse.from_dict(ai_orders_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


