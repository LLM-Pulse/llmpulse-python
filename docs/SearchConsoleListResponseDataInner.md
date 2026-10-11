# SearchConsoleListResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | The query or page URL | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 

## Example

```python
from llmpulse.models.search_console_list_response_data_inner import SearchConsoleListResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleListResponseDataInner from a JSON string
search_console_list_response_data_inner_instance = SearchConsoleListResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleListResponseDataInner.to_json())

# convert the object into a dict
search_console_list_response_data_inner_dict = search_console_list_response_data_inner_instance.to_dict()
# create an instance of SearchConsoleListResponseDataInner from a dict
search_console_list_response_data_inner_from_dict = SearchConsoleListResponseDataInner.from_dict(search_console_list_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


