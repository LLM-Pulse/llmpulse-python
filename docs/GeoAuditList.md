# GeoAuditList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[GeoAudit]**](GeoAudit.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_list import GeoAuditList

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditList from a JSON string
geo_audit_list_instance = GeoAuditList.from_json(json)
# print the JSON string representation of the object
print(GeoAuditList.to_json())

# convert the object into a dict
geo_audit_list_dict = geo_audit_list_instance.to_dict()
# create an instance of GeoAuditList from a dict
geo_audit_list_from_dict = GeoAuditList.from_dict(geo_audit_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


