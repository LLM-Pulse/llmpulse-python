# SearchConsoleProperty


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Property id, e.g. sc-domain:example.com | [optional] 
**name** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.search_console_property import SearchConsoleProperty

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleProperty from a JSON string
search_console_property_instance = SearchConsoleProperty.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleProperty.to_json())

# convert the object into a dict
search_console_property_dict = search_console_property_instance.to_dict()
# create an instance of SearchConsoleProperty from a dict
search_console_property_from_dict = SearchConsoleProperty.from_dict(search_console_property_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


