# GeoAuditFinding


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**check_key** | **str** | Stable key of the check within its audit type | [optional] 
**check_title** | **str** |  | [optional] 
**subject_key** | **str** | What the check is about (site for site-wide checks, a bot slug for robots.txt bot checks) | [optional] 
**subject** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**severity** | **str** |  | [optional] 
**evidence** | **object** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_finding import GeoAuditFinding

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditFinding from a JSON string
geo_audit_finding_instance = GeoAuditFinding.from_json(json)
# print the JSON string representation of the object
print(GeoAuditFinding.to_json())

# convert the object into a dict
geo_audit_finding_dict = geo_audit_finding_instance.to_dict()
# create an instance of GeoAuditFinding from a dict
geo_audit_finding_from_dict = GeoAuditFinding.from_dict(geo_audit_finding_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


