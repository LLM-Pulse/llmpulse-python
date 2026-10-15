# SuggestedPrompt


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**prompt** | **str** |  | 
**source** | **str** | The generator that wrote it: website, magic (keyword runs), topic, reddit, paa, reputational, translate, gsc (Search Console) or catalog | 
**status** | **str** | pending, accepted or rejected | 
**country_code** | **str** |  | 
**language_code** | **str** |  | 
**prompt_id** | **int** | The prompt an accepted suggestion became | 
**accepted_at** | **datetime** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from llmpulse.models.suggested_prompt import SuggestedPrompt

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestedPrompt from a JSON string
suggested_prompt_instance = SuggestedPrompt.from_json(json)
# print the JSON string representation of the object
print(SuggestedPrompt.to_json())

# convert the object into a dict
suggested_prompt_dict = suggested_prompt_instance.to_dict()
# create an instance of SuggestedPrompt from a dict
suggested_prompt_from_dict = SuggestedPrompt.from_dict(suggested_prompt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


