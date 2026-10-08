# GeoAuditArchived


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**id** | **str** |  | [optional] 
**archived** | **bool** |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_archived import GeoAuditArchived

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditArchived from a JSON string
geo_audit_archived_instance = GeoAuditArchived.from_json(json)
# print the JSON string representation of the object
print(GeoAuditArchived.to_json())

# convert the object into a dict
geo_audit_archived_dict = geo_audit_archived_instance.to_dict()
# create an instance of GeoAuditArchived from a dict
geo_audit_archived_from_dict = GeoAuditArchived.from_dict(geo_audit_archived_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


