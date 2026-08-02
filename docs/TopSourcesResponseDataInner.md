# TopSourcesResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** |  | [optional] 
**total_responses** | **int** |  | [optional] 
**avg_visibility** | **float** |  | [optional] 
**avg_mention_rate** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.top_sources_response_data_inner import TopSourcesResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of TopSourcesResponseDataInner from a JSON string
top_sources_response_data_inner_instance = TopSourcesResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(TopSourcesResponseDataInner.to_json())

# convert the object into a dict
top_sources_response_data_inner_dict = top_sources_response_data_inner_instance.to_dict()
# create an instance of TopSourcesResponseDataInner from a dict
top_sources_response_data_inner_from_dict = TopSourcesResponseDataInner.from_dict(top_sources_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


