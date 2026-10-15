# CompetitorSuggestion


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The suggestion key (brands) or the id of one citing source row (citations) | 
**domain** | **str** |  | 
**brand_name** | **str** | The proposed brand name; null for a cited domain | [optional] 
**matching_names** | **List[str]** | The names a tracked competitor would be matched by; empty for a cited domain | 
**mentions** | **int** | Answers naming the brand, when the discovery counted them (brands only) | [optional] 
**citations** | **int** | Answers citing the domain (citations only) | [optional] 

## Example

```python
from llmpulse.models.competitor_suggestion import CompetitorSuggestion

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorSuggestion from a JSON string
competitor_suggestion_instance = CompetitorSuggestion.from_json(json)
# print the JSON string representation of the object
print(CompetitorSuggestion.to_json())

# convert the object into a dict
competitor_suggestion_dict = competitor_suggestion_instance.to_dict()
# create an instance of CompetitorSuggestion from a dict
competitor_suggestion_from_dict = CompetitorSuggestion.from_dict(competitor_suggestion_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


