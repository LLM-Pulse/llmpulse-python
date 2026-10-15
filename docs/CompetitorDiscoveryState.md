# CompetitorDiscoveryState


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** | The last discovery run: pending, processing, completed or failed; null when none ever ran | [optional] 
**loading** | **bool** | A discovery run is in progress | 
**generated_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.competitor_discovery_state import CompetitorDiscoveryState

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorDiscoveryState from a JSON string
competitor_discovery_state_instance = CompetitorDiscoveryState.from_json(json)
# print the JSON string representation of the object
print(CompetitorDiscoveryState.to_json())

# convert the object into a dict
competitor_discovery_state_dict = competitor_discovery_state_instance.to_dict()
# create an instance of CompetitorDiscoveryState from a dict
competitor_discovery_state_from_dict = CompetitorDiscoveryState.from_dict(competitor_discovery_state_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


