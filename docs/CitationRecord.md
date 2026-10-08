# CitationRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** | The project&#39;s brand name (its name when no brand name is set) | 
**domain** | **str** | Host of the cited URL without www.; null when the URL has no parsable host | 
**prompt_id** | **int** |  | 
**prompt_execution_id** | **int** |  | 
**url** | **str** | Normalized cited URL (tracking parameters and fragment removed) | 
**position** | **int** | Rank of the citation in the answer; 0 for a background source reference with no visible rank | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.citation_record import CitationRecord

# TODO update the JSON string below
json = "{}"
# create an instance of CitationRecord from a JSON string
citation_record_instance = CitationRecord.from_json(json)
# print the JSON string representation of the object
print(CitationRecord.to_json())

# convert the object into a dict
citation_record_dict = citation_record_instance.to_dict()
# create an instance of CitationRecord from a dict
citation_record_from_dict = CitationRecord.from_dict(citation_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


