# ListWebhooks200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**project_id** | **int** |  | [optional] 
**event_type** | **str** |  | [optional] 
**target_url** | **str** |  | [optional] 
**disabled** | **bool** |  | [optional] 
**failure_count** | **int** |  | [optional] 
**last_delivered_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.list_webhooks200_response_data_inner import ListWebhooks200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListWebhooks200ResponseDataInner from a JSON string
list_webhooks200_response_data_inner_instance = ListWebhooks200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(ListWebhooks200ResponseDataInner.to_json())

# convert the object into a dict
list_webhooks200_response_data_inner_dict = list_webhooks200_response_data_inner_instance.to_dict()
# create an instance of ListWebhooks200ResponseDataInner from a dict
list_webhooks200_response_data_inner_from_dict = ListWebhooks200ResponseDataInner.from_dict(list_webhooks200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


