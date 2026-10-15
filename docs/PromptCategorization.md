# PromptCategorization


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**raw_input** | **str** |  | 
**prompt_type** | **str** |  | [optional] 
**brand_kind** | **str** |  | [optional] 
**categorization_source** | **str** | manual after an edit by hand; the prompt page&#39;s revert hands it back to automatic categorization | [optional] 
**manually_categorized** | **bool** |  | 
**categorized_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.prompt_categorization import PromptCategorization

# TODO update the JSON string below
json = "{}"
# create an instance of PromptCategorization from a JSON string
prompt_categorization_instance = PromptCategorization.from_json(json)
# print the JSON string representation of the object
print(PromptCategorization.to_json())

# convert the object into a dict
prompt_categorization_dict = prompt_categorization_instance.to_dict()
# create an instance of PromptCategorization from a dict
prompt_categorization_from_dict = PromptCategorization.from_dict(prompt_categorization_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


