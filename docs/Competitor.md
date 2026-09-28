# Competitor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**domain** | **str** | Bare (scheme-less) domain. Null only on the own-brand row (include_project_brand&#x3D;true) when the project has no URL. | [optional] 
**actor_type** | **str** | Only present when include_project_brand&#x3D;true | [optional] 
**is_own** | **bool** | Only present when include_project_brand&#x3D;true | [optional] 

## Example

```python
from llmpulse.models.competitor import Competitor

# TODO update the JSON string below
json = "{}"
# create an instance of Competitor from a JSON string
competitor_instance = Competitor.from_json(json)
# print the JSON string representation of the object
print(Competitor.to_json())

# convert the object into a dict
competitor_dict = competitor_instance.to_dict()
# create an instance of Competitor from a dict
competitor_from_dict = Competitor.from_dict(competitor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


