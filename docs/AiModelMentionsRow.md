# AiModelMentionsRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** | AI model key, as /dimensions/models lists it | [optional] 
**label** | **str** | Display name of the model | [optional] 
**color** | **str** | Hex color the app charts the model with | [optional] 
**mentions_count** | **int** | Brand mentions in the model&#39;s answers; 0 when it has none | [optional] 
**share_of_total** | **float** | The model&#39;s percentage (0-100) of total_mentions; null when total_mentions is 0 | [optional] 

## Example

```python
from llmpulse.models.ai_model_mentions_row import AiModelMentionsRow

# TODO update the JSON string below
json = "{}"
# create an instance of AiModelMentionsRow from a JSON string
ai_model_mentions_row_instance = AiModelMentionsRow.from_json(json)
# print the JSON string representation of the object
print(AiModelMentionsRow.to_json())

# convert the object into a dict
ai_model_mentions_row_dict = ai_model_mentions_row_instance.to_dict()
# create an instance of AiModelMentionsRow from a dict
ai_model_mentions_row_from_dict = AiModelMentionsRow.from_dict(ai_model_mentions_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


