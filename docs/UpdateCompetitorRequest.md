# UpdateCompetitorRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**brand_name** | **str** |  | [optional] 
**domain** | **str** | Website domain or host used for citation matching. A full URL is accepted and normalised to its host. | [optional] 
**matching_names** | **List[str]** |  | [optional] 
**color** | **str** | Hex color, e.g. #1a2b3c | [optional] 
**citation_match_mode** | **str** |  | [optional] 
**citation_match_path** | **str** | Required when changing citation_match_mode to path_prefix | [optional] 

## Example

```python
from llmpulse.models.update_competitor_request import UpdateCompetitorRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateCompetitorRequest from a JSON string
update_competitor_request_instance = UpdateCompetitorRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateCompetitorRequest.to_json())

# convert the object into a dict
update_competitor_request_dict = update_competitor_request_instance.to_dict()
# create an instance of UpdateCompetitorRequest from a dict
update_competitor_request_from_dict = UpdateCompetitorRequest.from_dict(update_competitor_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


