# QueryFanOutsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**view** | **str** | query or prompt, the row shape of data | 
**total_occurrences** | **int** | Sub-query occurrences across every page (view&#x3D;query) | [optional] 
**data** | [**List[QueryFanOutRow]**](QueryFanOutRow.md) |  | 

## Example

```python
from llmpulse.models.query_fan_outs_response import QueryFanOutsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of QueryFanOutsResponse from a JSON string
query_fan_outs_response_instance = QueryFanOutsResponse.from_json(json)
# print the JSON string representation of the object
print(QueryFanOutsResponse.to_json())

# convert the object into a dict
query_fan_outs_response_dict = query_fan_outs_response_instance.to_dict()
# create an instance of QueryFanOutsResponse from a dict
query_fan_outs_response_from_dict = QueryFanOutsResponse.from_dict(query_fan_outs_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


