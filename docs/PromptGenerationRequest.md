# PromptGenerationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**source** | **str** | Which Add prompts generator to run | 
**query** | **str** | keyword: optional keyword or research query. topic and reddit: required topic (reddit: the brand when search_type&#x3D;brand). paa: one keyword, as an alternative to keywords. | [optional] 
**count** | **int** | keyword and topic: how many suggestions to ask for, capped by the prompt slots left | [optional] [default to 20]
**country_code** | **str** | ISO 3166-1 alpha-2 country of the suggestions (default the project country) | [optional] 
**language_code** | **str** | ISO language code of the suggestions (default the project language) | [optional] 
**competitor_id** | **int** | keyword: write the suggestions around this competitor of the project | [optional] 
**search_type** | **str** | reddit: search discussions of a topic or a brand | [optional] [default to 'topic']
**keywords** | **List[str]** | paa: up to 5 keywords; each is a People Also Ask lookup counted against the account&#39;s 24-hour allowance | [optional] 
**source_country_code** | **str** | translate: country of the prompts to translate | [optional] 
**source_language_code** | **str** | translate: language of the prompts to translate | [optional] 
**min_words** | **int** | search_console: skip queries shorter than this many words | [optional] [default to 0]
**all_countries** | **bool** | search_console: include queries from every country instead of country_code only | [optional] [default to False]

## Example

```python
from llmpulse.models.prompt_generation_request import PromptGenerationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PromptGenerationRequest from a JSON string
prompt_generation_request_instance = PromptGenerationRequest.from_json(json)
# print the JSON string representation of the object
print(PromptGenerationRequest.to_json())

# convert the object into a dict
prompt_generation_request_dict = prompt_generation_request_instance.to_dict()
# create an instance of PromptGenerationRequest from a dict
prompt_generation_request_from_dict = PromptGenerationRequest.from_dict(prompt_generation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


