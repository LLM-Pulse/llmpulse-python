# GeoAuditSchedule

Present for weekly and monthly audits. day is 0 (Sunday) to 6 for weekly audits and 1 to 28 for monthly ones; hour is in timezone.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**day** | **int** |  | [optional] 
**hour** | **int** |  | [optional] 
**timezone** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_schedule import GeoAuditSchedule

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditSchedule from a JSON string
geo_audit_schedule_instance = GeoAuditSchedule.from_json(json)
# print the JSON string representation of the object
print(GeoAuditSchedule.to_json())

# convert the object into a dict
geo_audit_schedule_dict = geo_audit_schedule_instance.to_dict()
# create an instance of GeoAuditSchedule from a dict
geo_audit_schedule_from_dict = GeoAuditSchedule.from_dict(geo_audit_schedule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


