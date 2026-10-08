# TopSourcesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**filters** | [**MetricsFiltersEcho**](MetricsFiltersEcho.md) |  | [optional] 
**sort** | **str** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[TopSourcesResponseDataInner]**](TopSourcesResponseDataInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.top_sources_response import TopSourcesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TopSourcesResponse from a JSON string
top_sources_response_instance = TopSourcesResponse.from_json(json)
# print the JSON string representation of the object
print(TopSourcesResponse.to_json())

# convert the object into a dict
top_sources_response_dict = top_sources_response_instance.to_dict()
# create an instance of TopSourcesResponse from a dict
top_sources_response_from_dict = TopSourcesResponse.from_dict(top_sources_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


