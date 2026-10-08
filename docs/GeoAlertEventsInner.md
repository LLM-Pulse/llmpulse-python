# GeoAlertEventsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **str** |  | [optional] 
**check_key** | **str** |  | [optional] 
**subject_key** | **str** |  | [optional] 
**severity** | **str** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_alert_events_inner import GeoAlertEventsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAlertEventsInner from a JSON string
geo_alert_events_inner_instance = GeoAlertEventsInner.from_json(json)
# print the JSON string representation of the object
print(GeoAlertEventsInner.to_json())

# convert the object into a dict
geo_alert_events_inner_dict = geo_alert_events_inner_instance.to_dict()
# create an instance of GeoAlertEventsInner from a dict
geo_alert_events_inner_from_dict = GeoAlertEventsInner.from_dict(geo_alert_events_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


