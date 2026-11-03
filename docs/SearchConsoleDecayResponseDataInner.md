# SearchConsoleDecayResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | The page URL or query | [optional] 
**clicks** | **int** |  | [optional] 
**clicks_previous** | **int** |  | [optional] 
**clicks_change** | **int** | clicks minus clicks_previous (negative) | [optional] 
**clicks_change_pct** | **float** |  | [optional] 
**impressions** | **int** |  | [optional] 
**impressions_previous** | **int** |  | [optional] 
**position** | **float** | Null when the key had no impressions in the window | [optional] 
**position_previous** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.search_console_decay_response_data_inner import SearchConsoleDecayResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleDecayResponseDataInner from a JSON string
search_console_decay_response_data_inner_instance = SearchConsoleDecayResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleDecayResponseDataInner.to_json())

# convert the object into a dict
search_console_decay_response_data_inner_dict = search_console_decay_response_data_inner_instance.to_dict()
# create an instance of SearchConsoleDecayResponseDataInner from a dict
search_console_decay_response_data_inner_from_dict = SearchConsoleDecayResponseDataInner.from_dict(search_console_decay_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


