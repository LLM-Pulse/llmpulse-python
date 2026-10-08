# PromptSummaryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**filters** | [**MetricsFiltersEcho**](MetricsFiltersEcho.md) |  | [optional] 
**breakdown** | **str** |  | [optional] 
**sort** | **str** |  | [optional] 
**sort_dir** | **str** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[PromptSummaryRow]**](PromptSummaryRow.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.prompt_summary_response import PromptSummaryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PromptSummaryResponse from a JSON string
prompt_summary_response_instance = PromptSummaryResponse.from_json(json)
# print the JSON string representation of the object
print(PromptSummaryResponse.to_json())

# convert the object into a dict
prompt_summary_response_dict = prompt_summary_response_instance.to_dict()
# create an instance of PromptSummaryResponse from a dict
prompt_summary_response_from_dict = PromptSummaryResponse.from_dict(prompt_summary_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


