# SearchConsolePropertiesResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Property id, the value the property parameter takes, e.g. sc-domain:example.com | [optional] 
**name** | **str** |  | [optional] 
**primary** | **bool** | The property read when the property parameter is omitted | [optional] 
**type** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**last_synced_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.search_console_properties_response_data_inner import SearchConsolePropertiesResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsolePropertiesResponseDataInner from a JSON string
search_console_properties_response_data_inner_instance = SearchConsolePropertiesResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsolePropertiesResponseDataInner.to_json())

# convert the object into a dict
search_console_properties_response_data_inner_dict = search_console_properties_response_data_inner_instance.to_dict()
# create an instance of SearchConsolePropertiesResponseDataInner from a dict
search_console_properties_response_data_inner_from_dict = SearchConsolePropertiesResponseDataInner.from_dict(search_console_properties_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


