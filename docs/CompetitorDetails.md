# CompetitorDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**project_id** | **int** |  | [optional] 
**brand_name** | **str** |  | [optional] 
**domain** | **str** |  | [optional] 
**matching_names** | **List[str]** |  | [optional] 
**google_play_id** | **str** |  | [optional] 
**app_store_id** | **str** |  | [optional] 
**color** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.competitor_details import CompetitorDetails

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorDetails from a JSON string
competitor_details_instance = CompetitorDetails.from_json(json)
# print the JSON string representation of the object
print(CompetitorDetails.to_json())

# convert the object into a dict
competitor_details_dict = competitor_details_instance.to_dict()
# create an instance of CompetitorDetails from a dict
competitor_details_from_dict = CompetitorDetails.from_dict(competitor_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


