# CitationIntelligenceFiltersEcho

The filters the response was computed with, as the server resolved them. A filter that was not given is left out.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** |  | [optional] 
**collection_id** | **str** | The collection_id parameter as sent (one id or a comma-separated list) | [optional] 
**collection_ids** | **List[int]** |  | [optional] 
**domains** | **List[str]** | Lowercased domains | [optional] 
**prompt** | **int** | The prompt id filter | [optional] 
**brand_kind** | **str** |  | [optional] 
**country_code** | **str** |  | [optional] 
**language_code** | **str** |  | [optional] 
**var_from** | **str** | As given | [optional] 
**to** | **str** | As given | [optional] 
**key** | **str** | The group key, as matched | [optional] 
**query** | **str** |  | [optional] 
**source_type** | **str** |  | [optional] 
**sentiment** | **str** |  | [optional] 
**content_gap** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.citation_intelligence_filters_echo import CitationIntelligenceFiltersEcho

# TODO update the JSON string below
json = "{}"
# create an instance of CitationIntelligenceFiltersEcho from a JSON string
citation_intelligence_filters_echo_instance = CitationIntelligenceFiltersEcho.from_json(json)
# print the JSON string representation of the object
print(CitationIntelligenceFiltersEcho.to_json())

# convert the object into a dict
citation_intelligence_filters_echo_dict = citation_intelligence_filters_echo_instance.to_dict()
# create an instance of CitationIntelligenceFiltersEcho from a dict
citation_intelligence_filters_echo_from_dict = CitationIntelligenceFiltersEcho.from_dict(citation_intelligence_filters_echo_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


