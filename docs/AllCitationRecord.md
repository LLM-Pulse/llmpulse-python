# AllCitationRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The citation&#39;s id, unique within its actor_type | 
**actor_type** | **str** | project (your brand) or competitor | 
**competitor_id** | **int** | Competitor rows only | [optional] 
**name** | **str** | The project&#39;s brand name (its name when no brand name is set), or the competitor&#39;s brand name | 
**domain** | **str** | On project rows the host of the cited URL without www. (null when it has no parsable host); on competitor rows the competitor&#39;s bare domain | 
**prompt_id** | **int** |  | 
**prompt_execution_id** | **int** |  | 
**url** | **str** | Normalized cited URL (tracking parameters and fragment removed) | 
**position** | **int** | Rank of the citation in the answer; 0 for a background source reference with no visible rank | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.all_citation_record import AllCitationRecord

# TODO update the JSON string below
json = "{}"
# create an instance of AllCitationRecord from a JSON string
all_citation_record_instance = AllCitationRecord.from_json(json)
# print the JSON string representation of the object
print(AllCitationRecord.to_json())

# convert the object into a dict
all_citation_record_dict = all_citation_record_instance.to_dict()
# create an instance of AllCitationRecord from a dict
all_citation_record_from_dict = AllCitationRecord.from_dict(all_citation_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


