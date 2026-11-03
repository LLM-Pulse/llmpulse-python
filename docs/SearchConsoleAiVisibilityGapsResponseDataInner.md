# SearchConsoleAiVisibilityGapsResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** |  | [optional] 
**impressions** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**ctr** | **float** | 0..1 fraction | [optional] 
**position** | **float** | Impression-weighted average position | [optional] 
**prompt_id** | **int** | The project&#39;s prompt with the same text as the query; null when no prompt matches | [optional] 
**responses** | **int** | AI answers the matching prompt got in the window over the account&#39;s enabled models; null when no prompt matches | [optional] 
**brand_visibility** | **float** | Brand Visibility of the matching prompt in the window, percent (0-100) of its AI answers that mention the brand, over the account&#39;s enabled models; null when no prompt matches or it has no answer | [optional] 

## Example

```python
from llmpulse.models.search_console_ai_visibility_gaps_response_data_inner import SearchConsoleAiVisibilityGapsResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleAiVisibilityGapsResponseDataInner from a JSON string
search_console_ai_visibility_gaps_response_data_inner_instance = SearchConsoleAiVisibilityGapsResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleAiVisibilityGapsResponseDataInner.to_json())

# convert the object into a dict
search_console_ai_visibility_gaps_response_data_inner_dict = search_console_ai_visibility_gaps_response_data_inner_instance.to_dict()
# create an instance of SearchConsoleAiVisibilityGapsResponseDataInner from a dict
search_console_ai_visibility_gaps_response_data_inner_from_dict = SearchConsoleAiVisibilityGapsResponseDataInner.from_dict(search_console_ai_visibility_gaps_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


