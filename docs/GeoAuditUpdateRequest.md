# GeoAuditUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**cadence** | **str** |  | [optional] 
**schedule_day** | **int** | Weekly: 0 (Sunday) to 6. Monthly: 1 to 28. | [optional] 
**schedule_hour** | **int** | Hour of the day, 0 to 23, in the audit time zone | [optional] 
**status** | **str** | paused stops scheduled runs, active resumes them, archived is the same as DELETE | [optional] 
**email_alerts** | **bool** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_update_request import GeoAuditUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditUpdateRequest from a JSON string
geo_audit_update_request_instance = GeoAuditUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(GeoAuditUpdateRequest.to_json())

# convert the object into a dict
geo_audit_update_request_dict = geo_audit_update_request_instance.to_dict()
# create an instance of GeoAuditUpdateRequest from a dict
geo_audit_update_request_from_dict = GeoAuditUpdateRequest.from_dict(geo_audit_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


