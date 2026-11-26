# SourceRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**prompt_execution_id** | **int** |  | 
**domain** | **str** | Registrable domain of the cited URL | 
**url** | **str** | Normalized cited URL (tracking parameters and fragment removed) | 
**url_sha256** | **str** | Key of the cited page, as GET /citation_intelligence/urls/{url_sha256} takes it | 
**position** | **int** | Rank of the citation in the answer; 0 for a background source reference with no visible rank | 
**source_type** | **str** | owned (the project&#39;s domains), competitor or third_party | 
**is_google_play_link** | **bool** |  | 
**is_app_store_link** | **bool** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.source_record import SourceRecord

# TODO update the JSON string below
json = "{}"
# create an instance of SourceRecord from a JSON string
source_record_instance = SourceRecord.from_json(json)
# print the JSON string representation of the object
print(SourceRecord.to_json())

# convert the object into a dict
source_record_dict = source_record_instance.to_dict()
# create an instance of SourceRecord from a dict
source_record_from_dict = SourceRecord.from_dict(source_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


