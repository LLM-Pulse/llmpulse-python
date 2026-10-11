# SearchConsoleRowsResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | [optional] 
**country** | **str** |  | [optional] 
**device** | **str** |  | [optional] 
**page** | **str** |  | [optional] 
**query** | **str** |  | [optional] 
**search_appearance** | **str** |  | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 

## Example

```python
from llmpulse.models.search_console_rows_response_data_inner import SearchConsoleRowsResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleRowsResponseDataInner from a JSON string
search_console_rows_response_data_inner_instance = SearchConsoleRowsResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleRowsResponseDataInner.to_json())

# convert the object into a dict
search_console_rows_response_data_inner_dict = search_console_rows_response_data_inner_instance.to_dict()
# create an instance of SearchConsoleRowsResponseDataInner from a dict
search_console_rows_response_data_inner_from_dict = SearchConsoleRowsResponseDataInner.from_dict(search_console_rows_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


