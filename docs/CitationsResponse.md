# CitationsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[CitationRecord]**](CitationRecord.md) |  | 

## Example

```python
from llmpulse.models.citations_response import CitationsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CitationsResponse from a JSON string
citations_response_instance = CitationsResponse.from_json(json)
# print the JSON string representation of the object
print(CitationsResponse.to_json())

# convert the object into a dict
citations_response_dict = citations_response_instance.to_dict()
# create an instance of CitationsResponse from a dict
citations_response_from_dict = CitationsResponse.from_dict(citations_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


