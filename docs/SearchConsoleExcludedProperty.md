# SearchConsoleExcludedProperty


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**covered_by** | **str** | The selected property that already counts this one | [optional] 

## Example

```python
from llmpulse.models.search_console_excluded_property import SearchConsoleExcludedProperty

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleExcludedProperty from a JSON string
search_console_excluded_property_instance = SearchConsoleExcludedProperty.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleExcludedProperty.to_json())

# convert the object into a dict
search_console_excluded_property_dict = search_console_excluded_property_instance.to_dict()
# create an instance of SearchConsoleExcludedProperty from a dict
search_console_excluded_property_from_dict = SearchConsoleExcludedProperty.from_dict(search_console_excluded_property_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


