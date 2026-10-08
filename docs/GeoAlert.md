# GeoAlert


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**audit_id** | **str** |  | [optional] 
**audit_type** | **str** |  | [optional] 
**target** | **str** |  | [optional] 
**run_sequence** | **int** |  | [optional] 
**severity** | **str** |  | [optional] 
**events** | [**List[GeoAlertEventsInner]**](GeoAlertEventsInner.md) |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**app_url** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_alert import GeoAlert

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAlert from a JSON string
geo_alert_instance = GeoAlert.from_json(json)
# print the JSON string representation of the object
print(GeoAlert.to_json())

# convert the object into a dict
geo_alert_dict = geo_alert_instance.to_dict()
# create an instance of GeoAlert from a dict
geo_alert_from_dict = GeoAlert.from_dict(geo_alert_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


