# AiTrafficResponse

Visits from AI assistants measured by the connected web analytics provider, by day over the window.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**provider** | **str** | The connected provider: google_analytics, adobe_analytics, adobe_cja, posthog, plausible, matomo or piano | 
**var_from** | **date** |  | 
**to** | **date** |  | 
**granularity** | **str** |  | 
**totals** | [**AiTrafficResponseTotals**](AiTrafficResponseTotals.md) |  | 
**by_source** | [**List[AiTrafficResponseBySourceInner]**](AiTrafficResponseBySourceInner.md) | One row per AI source with traffic in the window, most sessions first | 
**timeseries** | **Dict[str, Dict[str, int]]** | Sessions keyed by AI source slug, then by the first day of the period (YYYY-MM-DD); a period without traffic is left out | 
**request_id** | **str** |  | 

## Example

```python
from llmpulse.models.ai_traffic_response import AiTrafficResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AiTrafficResponse from a JSON string
ai_traffic_response_instance = AiTrafficResponse.from_json(json)
# print the JSON string representation of the object
print(AiTrafficResponse.to_json())

# convert the object into a dict
ai_traffic_response_dict = ai_traffic_response_instance.to_dict()
# create an instance of AiTrafficResponse from a dict
ai_traffic_response_from_dict = AiTrafficResponse.from_dict(ai_traffic_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


