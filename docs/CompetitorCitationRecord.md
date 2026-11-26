# CompetitorCitationRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**competitor_id** | **int** |  | 
**name** | **str** | The competitor&#39;s brand name | 
**domain** | **str** | The competitor&#39;s bare domain | 
**prompt_execution_id** | **int** |  | 
**url** | **str** | Normalized cited URL (tracking parameters and fragment removed) | 
**position** | **int** | Rank of the citation in the answer; 0 for a background source reference with no visible rank | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.competitor_citation_record import CompetitorCitationRecord

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorCitationRecord from a JSON string
competitor_citation_record_instance = CompetitorCitationRecord.from_json(json)
# print the JSON string representation of the object
print(CompetitorCitationRecord.to_json())

# convert the object into a dict
competitor_citation_record_dict = competitor_citation_record_instance.to_dict()
# create an instance of CompetitorCitationRecord from a dict
competitor_citation_record_from_dict = CompetitorCitationRecord.from_dict(competitor_citation_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


