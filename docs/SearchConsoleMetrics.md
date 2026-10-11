# SearchConsoleMetrics


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 

## Example

```python
from llmpulse.models.search_console_metrics import SearchConsoleMetrics

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleMetrics from a JSON string
search_console_metrics_instance = SearchConsoleMetrics.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleMetrics.to_json())

# convert the object into a dict
search_console_metrics_dict = search_console_metrics_instance.to_dict()
# create an instance of SearchConsoleMetrics from a dict
search_console_metrics_from_dict = SearchConsoleMetrics.from_dict(search_console_metrics_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


