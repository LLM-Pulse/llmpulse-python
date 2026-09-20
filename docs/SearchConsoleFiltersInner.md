# SearchConsoleFiltersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dimension** | **str** |  | 
**operator** | **str** |  | [optional] [default to 'contains']
**expression** | **str** |  | 

## Example

```python
from llmpulse.models.search_console_filters_inner import SearchConsoleFiltersInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleFiltersInner from a JSON string
search_console_filters_inner_instance = SearchConsoleFiltersInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleFiltersInner.to_json())

# convert the object into a dict
search_console_filters_inner_dict = search_console_filters_inner_instance.to_dict()
# create an instance of SearchConsoleFiltersInner from a dict
search_console_filters_inner_from_dict = SearchConsoleFiltersInner.from_dict(search_console_filters_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


