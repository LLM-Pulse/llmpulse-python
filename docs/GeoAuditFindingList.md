# GeoAuditFindingList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[GeoAuditFinding]**](GeoAuditFinding.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_finding_list import GeoAuditFindingList

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditFindingList from a JSON string
geo_audit_finding_list_instance = GeoAuditFindingList.from_json(json)
# print the JSON string representation of the object
print(GeoAuditFindingList.to_json())

# convert the object into a dict
geo_audit_finding_list_dict = geo_audit_finding_list_instance.to_dict()
# create an instance of GeoAuditFindingList from a dict
geo_audit_finding_list_from_dict = GeoAuditFindingList.from_dict(geo_audit_finding_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


