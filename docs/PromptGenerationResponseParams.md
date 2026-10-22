# PromptGenerationResponseParams

The validated request the run uses, with the project's locale filled in

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country_code** | **str** |  | [optional] 
**language_code** | **str** |  | [optional] 
**query** | **str** |  | [optional] 
**count** | **int** |  | [optional] 
**competitor_id** | **int** |  | [optional] 
**search_type** | **str** |  | [optional] 
**keywords** | **List[str]** |  | [optional] 
**source_country_code** | **str** |  | [optional] 
**source_language_code** | **str** |  | [optional] 
**min_words** | **int** |  | [optional] 
**all_countries** | **bool** |  | [optional] 
**var_property** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.prompt_generation_response_params import PromptGenerationResponseParams

# TODO update the JSON string below
json = "{}"
# create an instance of PromptGenerationResponseParams from a JSON string
prompt_generation_response_params_instance = PromptGenerationResponseParams.from_json(json)
# print the JSON string representation of the object
print(PromptGenerationResponseParams.to_json())

# convert the object into a dict
prompt_generation_response_params_dict = prompt_generation_response_params_instance.to_dict()
# create an instance of PromptGenerationResponseParams from a dict
prompt_generation_response_params_from_dict = PromptGenerationResponseParams.from_dict(prompt_generation_response_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


