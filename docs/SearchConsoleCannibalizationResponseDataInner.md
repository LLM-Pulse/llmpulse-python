# SearchConsoleCannibalizationResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** |  | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 
**pages** | [**List[SearchConsoleCannibalizationResponseDataInnerPagesInner]**](SearchConsoleCannibalizationResponseDataInnerPagesInner.md) | Pages taking at least min_share of the query&#39;s impressions, most impressions first | [optional] 

## Example

```python
from llmpulse.models.search_console_cannibalization_response_data_inner import SearchConsoleCannibalizationResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleCannibalizationResponseDataInner from a JSON string
search_console_cannibalization_response_data_inner_instance = SearchConsoleCannibalizationResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleCannibalizationResponseDataInner.to_json())

# convert the object into a dict
search_console_cannibalization_response_data_inner_dict = search_console_cannibalization_response_data_inner_instance.to_dict()
# create an instance of SearchConsoleCannibalizationResponseDataInner from a dict
search_console_cannibalization_response_data_inner_from_dict = SearchConsoleCannibalizationResponseDataInner.from_dict(search_console_cannibalization_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


