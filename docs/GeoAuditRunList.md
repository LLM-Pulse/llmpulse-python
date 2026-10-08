# GeoAuditRunList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[GeoAuditRun]**](GeoAuditRun.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_run_list import GeoAuditRunList

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditRunList from a JSON string
geo_audit_run_list_instance = GeoAuditRunList.from_json(json)
# print the JSON string representation of the object
print(GeoAuditRunList.to_json())

# convert the object into a dict
geo_audit_run_list_dict = geo_audit_run_list_instance.to_dict()
# create an instance of GeoAuditRunList from a dict
geo_audit_run_list_from_dict = GeoAuditRunList.from_dict(geo_audit_run_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


