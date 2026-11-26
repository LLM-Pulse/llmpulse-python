# AllMentionRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The mention&#39;s id, unique within its actor_type | 
**actor_type** | **str** | project (your brand) or competitor | 
**competitor_id** | **int** | Competitor rows only | [optional] 
**name** | **str** | The project&#39;s brand name (its name when no brand name is set), or the competitor&#39;s brand name | 
**domain** | **str** | The competitor&#39;s bare domain (competitor rows only) | [optional] 
**prompt_id** | **int** |  | 
**prompt_execution_id** | **int** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.all_mention_record import AllMentionRecord

# TODO update the JSON string below
json = "{}"
# create an instance of AllMentionRecord from a JSON string
all_mention_record_instance = AllMentionRecord.from_json(json)
# print the JSON string representation of the object
print(AllMentionRecord.to_json())

# convert the object into a dict
all_mention_record_dict = all_mention_record_instance.to_dict()
# create an instance of AllMentionRecord from a dict
all_mention_record_from_dict = AllMentionRecord.from_dict(all_mention_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


