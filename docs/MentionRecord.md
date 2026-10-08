# MentionRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** | The project&#39;s brand name (its name when no brand name is set) | 
**prompt_id** | **int** |  | 
**prompt_execution_id** | **int** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.mention_record import MentionRecord

# TODO update the JSON string below
json = "{}"
# create an instance of MentionRecord from a JSON string
mention_record_instance = MentionRecord.from_json(json)
# print the JSON string representation of the object
print(MentionRecord.to_json())

# convert the object into a dict
mention_record_dict = mention_record_instance.to_dict()
# create an instance of MentionRecord from a dict
mention_record_from_dict = MentionRecord.from_dict(mention_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


