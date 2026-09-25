# PromptSummaryRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompt_id** | **int** |  | [optional] 
**prompt_text** | **str** |  | [optional] 
**model** | **str** | Only present when breakdown&#x3D;model | [optional] 
**responses** | **int** |  | [optional] 
**mentions** | **int** |  | [optional] 
**citations** | **int** |  | [optional] 
**visibility** | **float** |  | [optional] 
**mention_rate** | **float** |  | [optional] 
**citation_rate** | **float** |  | [optional] 
**avg_mention_position** | **float** |  | [optional] 
**avg_position** | **float** |  | [optional] 
**app_url** | **str** | Opens this prompt in the app. The link names its project, so it opens there for any user with access to that project | [optional] 

## Example

```python
from llmpulse.models.prompt_summary_row import PromptSummaryRow

# TODO update the JSON string below
json = "{}"
# create an instance of PromptSummaryRow from a JSON string
prompt_summary_row_instance = PromptSummaryRow.from_json(json)
# print the JSON string representation of the object
print(PromptSummaryRow.to_json())

# convert the object into a dict
prompt_summary_row_dict = prompt_summary_row_instance.to_dict()
# create an instance of PromptSummaryRow from a dict
prompt_summary_row_from_dict = PromptSummaryRow.from_dict(prompt_summary_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


