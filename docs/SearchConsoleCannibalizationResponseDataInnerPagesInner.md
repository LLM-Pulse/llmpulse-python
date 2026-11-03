# SearchConsoleCannibalizationResponseDataInnerPagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **str** |  | [optional] 
**share** | **float** | The page&#39;s fraction (0..1) of the query&#39;s impressions | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 

## Example

```python
from llmpulse.models.search_console_cannibalization_response_data_inner_pages_inner import SearchConsoleCannibalizationResponseDataInnerPagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleCannibalizationResponseDataInnerPagesInner from a JSON string
search_console_cannibalization_response_data_inner_pages_inner_instance = SearchConsoleCannibalizationResponseDataInnerPagesInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleCannibalizationResponseDataInnerPagesInner.to_json())

# convert the object into a dict
search_console_cannibalization_response_data_inner_pages_inner_dict = search_console_cannibalization_response_data_inner_pages_inner_instance.to_dict()
# create an instance of SearchConsoleCannibalizationResponseDataInnerPagesInner from a dict
search_console_cannibalization_response_data_inner_pages_inner_from_dict = SearchConsoleCannibalizationResponseDataInnerPagesInner.from_dict(search_console_cannibalization_response_data_inner_pages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


