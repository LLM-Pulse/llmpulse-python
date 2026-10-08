# GeoAuditIssue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**check_key** | **str** |  | [optional] 
**check_title** | **str** |  | [optional] 
**subject_key** | **str** |  | [optional] 
**subject** | **str** |  | [optional] 
**severity** | **str** |  | [optional] 
**state** | **str** |  | [optional] 
**badge** | **str** | How the latest comparable run moved the issue | [optional] 
**accepted** | **bool** |  | [optional] 
**accepted_at** | **datetime** |  | [optional] 
**regression_count** | **int** |  | [optional] 
**evidence** | **object** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_issue import GeoAuditIssue

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditIssue from a JSON string
geo_audit_issue_instance = GeoAuditIssue.from_json(json)
# print the JSON string representation of the object
print(GeoAuditIssue.to_json())

# convert the object into a dict
geo_audit_issue_dict = geo_audit_issue_instance.to_dict()
# create an instance of GeoAuditIssue from a dict
geo_audit_issue_from_dict = GeoAuditIssue.from_dict(geo_audit_issue_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


