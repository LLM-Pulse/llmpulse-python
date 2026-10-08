# CompetitorMentionRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**competitor_id** | **int** |  | 
**name** | **str** | The competitor&#39;s brand name | 
**domain** | **str** | The competitor&#39;s bare domain | 
**prompt_execution_id** | **int** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.competitor_mention_record import CompetitorMentionRecord

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorMentionRecord from a JSON string
competitor_mention_record_instance = CompetitorMentionRecord.from_json(json)
# print the JSON string representation of the object
print(CompetitorMentionRecord.to_json())

# convert the object into a dict
competitor_mention_record_dict = competitor_mention_record_instance.to_dict()
# create an instance of CompetitorMentionRecord from a dict
competitor_mention_record_from_dict = CompetitorMentionRecord.from_dict(competitor_mention_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


