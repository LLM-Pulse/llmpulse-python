# AiTrafficResponseTotals


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**users** | **int** |  | 
**sessions** | **int** |  | 
**conversions** | **int** |  | 
**conversion_rate** | **float** | conversions as a percentage (0-100) of sessions; 0 without sessions | 

## Example

```python
from llmpulse.models.ai_traffic_response_totals import AiTrafficResponseTotals

# TODO update the JSON string below
json = "{}"
# create an instance of AiTrafficResponseTotals from a JSON string
ai_traffic_response_totals_instance = AiTrafficResponseTotals.from_json(json)
# print the JSON string representation of the object
print(AiTrafficResponseTotals.to_json())

# convert the object into a dict
ai_traffic_response_totals_dict = ai_traffic_response_totals_instance.to_dict()
# create an instance of AiTrafficResponseTotals from a dict
ai_traffic_response_totals_from_dict = AiTrafficResponseTotals.from_dict(ai_traffic_response_totals_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


