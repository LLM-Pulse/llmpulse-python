# GeoAuditCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**data** | [**List[GeoAudit]**](GeoAudit.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_create_response import GeoAuditCreateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditCreateResponse from a JSON string
geo_audit_create_response_instance = GeoAuditCreateResponse.from_json(json)
# print the JSON string representation of the object
print(GeoAuditCreateResponse.to_json())

# convert the object into a dict
geo_audit_create_response_dict = geo_audit_create_response_instance.to_dict()
# create an instance of GeoAuditCreateResponse from a dict
geo_audit_create_response_from_dict = GeoAuditCreateResponse.from_dict(geo_audit_create_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


