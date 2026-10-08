# GeoAuditIssueResponse


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
**project_id** | **int** |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_issue_response import GeoAuditIssueResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditIssueResponse from a JSON string
geo_audit_issue_response_instance = GeoAuditIssueResponse.from_json(json)
# print the JSON string representation of the object
print(GeoAuditIssueResponse.to_json())

# convert the object into a dict
geo_audit_issue_response_dict = geo_audit_issue_response_instance.to_dict()
# create an instance of GeoAuditIssueResponse from a dict
geo_audit_issue_response_from_dict = GeoAuditIssueResponse.from_dict(geo_audit_issue_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


