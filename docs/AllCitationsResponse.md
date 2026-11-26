# AllCitationsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**data** | [**List[AllCitationRecord]**](AllCitationRecord.md) |  | 

## Example

```python
from llmpulse.models.all_citations_response import AllCitationsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AllCitationsResponse from a JSON string
all_citations_response_instance = AllCitationsResponse.from_json(json)
# print the JSON string representation of the object
print(AllCitationsResponse.to_json())

# convert the object into a dict
all_citations_response_dict = all_citations_response_instance.to_dict()
# create an instance of AllCitationsResponse from a dict
all_citations_response_from_dict = AllCitationsResponse.from_dict(all_citations_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


