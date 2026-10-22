# SearchConsolePropertiesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**max_properties** | **int** | How many properties a project can connect | [optional] 
**data** | [**List[SearchConsolePropertiesResponseDataInner]**](SearchConsolePropertiesResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.search_console_properties_response import SearchConsolePropertiesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchConsolePropertiesResponse from a JSON string
search_console_properties_response_instance = SearchConsolePropertiesResponse.from_json(json)
# print the JSON string representation of the object
print(SearchConsolePropertiesResponse.to_json())

# convert the object into a dict
search_console_properties_response_dict = search_console_properties_response_instance.to_dict()
# create an instance of SearchConsolePropertiesResponse from a dict
search_console_properties_response_from_dict = SearchConsolePropertiesResponse.from_dict(search_console_properties_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


