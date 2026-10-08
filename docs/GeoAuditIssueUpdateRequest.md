# GeoAuditIssueUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**accepted** | **bool** | true accepts the issue (it stays listed but leaves the open count until its evidence changes); false reopens it | 

## Example

```python
from llmpulse.models.geo_audit_issue_update_request import GeoAuditIssueUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditIssueUpdateRequest from a JSON string
geo_audit_issue_update_request_instance = GeoAuditIssueUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(GeoAuditIssueUpdateRequest.to_json())

# convert the object into a dict
geo_audit_issue_update_request_dict = geo_audit_issue_update_request_instance.to_dict()
# create an instance of GeoAuditIssueUpdateRequest from a dict
geo_audit_issue_update_request_from_dict = GeoAuditIssueUpdateRequest.from_dict(geo_audit_issue_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


