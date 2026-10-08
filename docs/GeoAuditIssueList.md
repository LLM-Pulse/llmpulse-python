# GeoAuditIssueList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[GeoAuditIssue]**](GeoAuditIssue.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_issue_list import GeoAuditIssueList

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditIssueList from a JSON string
geo_audit_issue_list_instance = GeoAuditIssueList.from_json(json)
# print the JSON string representation of the object
print(GeoAuditIssueList.to_json())

# convert the object into a dict
geo_audit_issue_list_dict = geo_audit_issue_list_instance.to_dict()
# create an instance of GeoAuditIssueList from a dict
geo_audit_issue_list_from_dict = GeoAuditIssueList.from_dict(geo_audit_issue_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


