# GeoAuditRunDetail


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sequence** | **int** | Run number within the audit, starting at 1 | [optional] 
**status** | **str** |  | [optional] 
**trigger** | **str** |  | [optional] 
**score** | **float** |  | [optional] 
**grade** | **str** |  | [optional] 
**score_delta** | **float** | Score change against the previous completed run | [optional] 
**comparable_to_previous** | **bool** | False when the checks or the audit settings changed since the previous run, so a diff may reflect that change | [optional] 
**new_issues** | **int** |  | [optional] 
**fixed_issues** | **int** |  | [optional] 
**regressed_issues** | **int** |  | [optional] 
**error** | **str** |  | [optional] 
**engine_version** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**finished_at** | **datetime** |  | [optional] 
**app_url** | **str** |  | [optional] 
**project_id** | **int** |  | [optional] 
**metrics** | **Dict[str, float]** |  | [optional] 
**result_data** | **object** | The full report of the run, in the shape of the matching technical GEO report type | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_audit_run_detail import GeoAuditRunDetail

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditRunDetail from a JSON string
geo_audit_run_detail_instance = GeoAuditRunDetail.from_json(json)
# print the JSON string representation of the object
print(GeoAuditRunDetail.to_json())

# convert the object into a dict
geo_audit_run_detail_dict = geo_audit_run_detail_instance.to_dict()
# create an instance of GeoAuditRunDetail from a dict
geo_audit_run_detail_from_dict = GeoAuditRunDetail.from_dict(geo_audit_run_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


