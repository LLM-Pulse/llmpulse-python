# PromptRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**prompt_text** | **str** |  | 
**collection_id** | **int** | Primary tag, when the prompt has one | 
**collection_ids** | **List[int]** | Every tag the prompt belongs to | 
**tags** | [**List[TagRef]**](TagRef.md) |  | 
**country_code** | **str** |  | 
**language_code** | **str** |  | 
**prompt_type** | **str** | Search intent: informational, navigational, commercial or transactional. Null until the prompt is classified | 
**brand_kind** | **str** | Brand focus: brand, brand_other or non_brand. Null until the prompt is classified | 
**last_executed_at** | **datetime** | Null until the prompt has run | 
**app_url** | **str** | Opens this prompt in the app. The link names its project, so it opens there for any user with access to that project | 

## Example

```python
from llmpulse.models.prompt_record import PromptRecord

# TODO update the JSON string below
json = "{}"
# create an instance of PromptRecord from a JSON string
prompt_record_instance = PromptRecord.from_json(json)
# print the JSON string representation of the object
print(PromptRecord.to_json())

# convert the object into a dict
prompt_record_dict = prompt_record_instance.to_dict()
# create an instance of PromptRecord from a dict
prompt_record_from_dict = PromptRecord.from_dict(prompt_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


