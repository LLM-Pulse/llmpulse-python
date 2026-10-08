# GeoAuditComparisonChangesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**check_key** | **str** |  | [optional] 
**check_title** | **str** |  | [optional] 
**subject_key** | **str** |  | [optional] 
**subject** | **str** |  | [optional] 
**severity** | **str** |  | [optional] 
**from_status** | **str** |  | [optional] 
**to_status** | **str** |  | [optional] 
**change** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_comparison_changes_inner import GeoAuditComparisonChangesInner

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditComparisonChangesInner from a JSON string
geo_audit_comparison_changes_inner_instance = GeoAuditComparisonChangesInner.from_json(json)
# print the JSON string representation of the object
print(GeoAuditComparisonChangesInner.to_json())

# convert the object into a dict
geo_audit_comparison_changes_inner_dict = geo_audit_comparison_changes_inner_instance.to_dict()
# create an instance of GeoAuditComparisonChangesInner from a dict
geo_audit_comparison_changes_inner_from_dict = GeoAuditComparisonChangesInner.from_dict(geo_audit_comparison_changes_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


