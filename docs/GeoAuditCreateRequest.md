# GeoAuditCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**target** | **str** | The domain (site-wide types) or page URL to audit | 
**audit_types** | **List[str]** | One or more audit types; each becomes its own audit and starts its first run | 
**cadence** | **str** | once (default), weekly or monthly. Weekly and monthly need a type whose checks are tracked and count against the plan limit of recurring audits | [optional] 

## Example

```python
from llmpulse.models.geo_audit_create_request import GeoAuditCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditCreateRequest from a JSON string
geo_audit_create_request_instance = GeoAuditCreateRequest.from_json(json)
# print the JSON string representation of the object
print(GeoAuditCreateRequest.to_json())

# convert the object into a dict
geo_audit_create_request_dict = geo_audit_create_request_instance.to_dict()
# create an instance of GeoAuditCreateRequest from a dict
geo_audit_create_request_from_dict = GeoAuditCreateRequest.from_dict(geo_audit_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


