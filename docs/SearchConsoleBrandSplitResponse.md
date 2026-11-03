# SearchConsoleBrandSplitResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_property** | [**SearchConsoleProperty**](SearchConsoleProperty.md) |  | [optional] 
**properties** | [**List[SearchConsoleProperty]**](SearchConsoleProperty.md) | With a list or all in the property parameter, the properties whose data the response holds (instead of property) | [optional] 
**excluded_properties** | [**List[SearchConsoleExcludedProperty]**](SearchConsoleExcludedProperty.md) | With a list or all, selected properties left out because another selected property already counts them | [optional] 
**property_errors** | [**List[SearchConsolePropertyError]**](SearchConsolePropertyError.md) | With a list or all, selected properties Google refused, left out of the figures | [optional] 
**var_from** | **date** |  | [optional] 
**to** | **date** |  | [optional] 
**data_through** | **date** | Latest date Google has published for the property, or for every combined property (it lags 2-3 days). Later days are missing, not zero. | [optional] 
**brand_terms** | **List[str]** | The project&#39;s brand name, matching names, app names and domain, lowercased, each matched as a whole word | [optional] 
**totals** | [**SearchConsoleMetrics**](SearchConsoleMetrics.md) |  | [optional] 
**branded** | [**SearchConsoleMetrics**](SearchConsoleMetrics.md) |  | [optional] 
**non_branded** | [**SearchConsoleMetrics**](SearchConsoleMetrics.md) |  | [optional] 
**unclassified** | [**SearchConsoleBrandSplitResponseUnclassified**](SearchConsoleBrandSplitResponseUnclassified.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.search_console_brand_split_response import SearchConsoleBrandSplitResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsoleBrandSplitResponse from a JSON string
search_console_brand_split_response_instance = SearchConsoleBrandSplitResponse.from_json(json)
# print the JSON string representation of the object
print(SearchConsoleBrandSplitResponse.to_json())

# convert the object into a dict
search_console_brand_split_response_dict = search_console_brand_split_response_instance.to_dict()
# create an instance of SearchConsoleBrandSplitResponse from a dict
search_console_brand_split_response_from_dict = SearchConsoleBrandSplitResponse.from_dict(search_console_brand_split_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


