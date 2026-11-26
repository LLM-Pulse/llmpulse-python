# CitationGroupsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**view** | **str** | url, domain or host | 
**filters** | [**CitationIntelligenceFiltersEcho**](CitationIntelligenceFiltersEcho.md) |  | 
**data** | [**List[CitationGroupRow]**](CitationGroupRow.md) |  | 

## Example

```python
from llmpulse.models.citation_groups_response import CitationGroupsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CitationGroupsResponse from a JSON string
citation_groups_response_instance = CitationGroupsResponse.from_json(json)
# print the JSON string representation of the object
print(CitationGroupsResponse.to_json())

# convert the object into a dict
citation_groups_response_dict = citation_groups_response_instance.to_dict()
# create an instance of CitationGroupsResponse from a dict
citation_groups_response_from_dict = CitationGroupsResponse.from_dict(citation_groups_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


