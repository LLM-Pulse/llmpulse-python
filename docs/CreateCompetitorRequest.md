# CreateCompetitorRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**brand_name** | **str** |  | 
**domain** | **str** | URL is accepted and normalised to host (e.g. https://www.openai.com → openai.com) | 
**matching_names** | **List[str]** |  | [optional] 

## Example

```python
from llmpulse.models.create_competitor_request import CreateCompetitorRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCompetitorRequest from a JSON string
create_competitor_request_instance = CreateCompetitorRequest.from_json(json)
# print the JSON string representation of the object
print(CreateCompetitorRequest.to_json())

# convert the object into a dict
create_competitor_request_dict = create_competitor_request_instance.to_dict()
# create an instance of CreateCompetitorRequest from a dict
create_competitor_request_from_dict = CreateCompetitorRequest.from_dict(create_competitor_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


