# SearchConsoleSummaryResponseBreakdownInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **str** |  | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 

## Example

```python
from llmpulse.models.search_console_summary_response_breakdown_inner import SearchConsoleSummaryResponseBreakdownInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleSummaryResponseBreakdownInner from a JSON string
search_console_summary_response_breakdown_inner_instance = SearchConsoleSummaryResponseBreakdownInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleSummaryResponseBreakdownInner.to_json())

# convert the object into a dict
search_console_summary_response_breakdown_inner_dict = search_console_summary_response_breakdown_inner_instance.to_dict()
# create an instance of SearchConsoleSummaryResponseBreakdownInner from a dict
search_console_summary_response_breakdown_inner_from_dict = SearchConsoleSummaryResponseBreakdownInner.from_dict(search_console_summary_response_breakdown_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


