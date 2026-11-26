# SourcesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[SourceRecord]**](SourceRecord.md) |  | 

## Example

```python
from llmpulse.models.sources_response import SourcesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SourcesResponse from a JSON string
sources_response_instance = SourcesResponse.from_json(json)
# print the JSON string representation of the object
print(SourcesResponse.to_json())

# convert the object into a dict
sources_response_dict = sources_response_instance.to_dict()
# create an instance of SourcesResponse from a dict
sources_response_from_dict = SourcesResponse.from_dict(sources_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


