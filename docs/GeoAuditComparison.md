# GeoAuditComparison


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**from_run** | [**GeoAuditRun**](GeoAuditRun.md) |  | [optional] 
**to_run** | [**GeoAuditRun**](GeoAuditRun.md) |  | [optional] 
**comparable** | **bool** |  | [optional] 
**score_delta** | **float** |  | [optional] 
**metric_deltas** | **Dict[str, float]** |  | [optional] 
**counts** | **Dict[str, int]** |  | [optional] 
**changes** | [**List[GeoAuditComparisonChangesInner]**](GeoAuditComparisonChangesInner.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_comparison import GeoAuditComparison

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditComparison from a JSON string
geo_audit_comparison_instance = GeoAuditComparison.from_json(json)
# print the JSON string representation of the object
print(GeoAuditComparison.to_json())

# convert the object into a dict
geo_audit_comparison_dict = geo_audit_comparison_instance.to_dict()
# create an instance of GeoAuditComparison from a dict
geo_audit_comparison_from_dict = GeoAuditComparison.from_dict(geo_audit_comparison_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


