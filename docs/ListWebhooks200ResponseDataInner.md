# ListWebhooks200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**project_id** | **int** |  | [optional] 
**event_type** | **str** |  | [optional] 
**target_url** | **str** | The URL deliveries are sent to. A read-only API key receives only its scheme, host and any non-default port followed by &#x60;/…&#x60; (for example &#x60;https://hook.eu1.make.com/…&#x60;); a &#x60;read_write&#x60; scope key receives the full URL. | [optional] 
**disabled** | **bool** | True when the subscription receives no more events, including when the API key or OAuth connection that created it was revoked, or when that API key is limited to some projects and no longer covers the subscription&#39;s project. Creating it again with the same project, event and URL replaces it with a new subscription and secret. | [optional] 
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


