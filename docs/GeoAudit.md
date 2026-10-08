# GeoAudit


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Stable audit id | [optional] 
**audit_type** | **str** |  | [optional] 
**target** | **str** | The audited domain (site-wide types) or page URL, normalized | [optional] 
**country_code** | **str** |  | [optional] 
**cadence** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**paused_reason** | **str** | user, or unreachable when three runs in a row could not reach the site | [optional] 
**schedule** | [**GeoAuditSchedule**](GeoAuditSchedule.md) |  | [optional] 
**next_run_at** | **datetime** |  | [optional] 
**email_alerts** | **bool** |  | [optional] 
**recurring_available** | **bool** | Whether this audit type can run weekly or monthly | [optional] 
**checks_tracked** | **bool** | Whether runs of this type produce findings and issues, or a score only | [optional] 
**latest_run** | [**GeoAuditRun**](GeoAuditRun.md) |  | [optional] 
**open_issues** | **int** |  | [optional] 
**open_critical_issues** | **int** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**app_url** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit import GeoAudit

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAudit from a JSON string
geo_audit_instance = GeoAudit.from_json(json)
# print the JSON string representation of the object
print(GeoAudit.to_json())

# convert the object into a dict
geo_audit_dict = geo_audit_instance.to_dict()
# create an instance of GeoAudit from a dict
geo_audit_from_dict = GeoAudit.from_dict(geo_audit_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


