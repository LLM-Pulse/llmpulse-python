# CompetitorCreateResponseCompetitor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**brand_name** | **str** |  | 
**domain** | **str** |  | 
**citation_match_mode** | [**CitationMatchMode**](CitationMatchMode.md) |  | 
**citation_match_path** | **str** | Set only when citation_match_mode is path_prefix | 
**color** | **str** |  | 
**matching_names** | **List[str]** |  | 

## Example

```python
from llmpulse.models.competitor_create_response_competitor import CompetitorCreateResponseCompetitor

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorCreateResponseCompetitor from a JSON string
competitor_create_response_competitor_instance = CompetitorCreateResponseCompetitor.from_json(json)
# print the JSON string representation of the object
print(CompetitorCreateResponseCompetitor.to_json())

# convert the object into a dict
competitor_create_response_competitor_dict = competitor_create_response_competitor_instance.to_dict()
# create an instance of CompetitorCreateResponseCompetitor from a dict
competitor_create_response_competitor_from_dict = CompetitorCreateResponseCompetitor.from_dict(competitor_create_response_competitor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


