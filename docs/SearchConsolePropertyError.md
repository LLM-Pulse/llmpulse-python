# SearchConsolePropertyError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**retry_after** | **int** | Seconds to wait before retrying, for ERR_SEARCH_CONSOLE_UPSTREAM | [optional] 

## Example

```python
from llmpulse.models.search_console_property_error import SearchConsolePropertyError

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsolePropertyError from a JSON string
search_console_property_error_instance = SearchConsolePropertyError.from_json(json)
# print the JSON string representation of the object
print(SearchConsolePropertyError.to_json())

# convert the object into a dict
search_console_property_error_dict = search_console_property_error_instance.to_dict()
# create an instance of SearchConsolePropertyError from a dict
search_console_property_error_from_dict = SearchConsolePropertyError.from_dict(search_console_property_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


