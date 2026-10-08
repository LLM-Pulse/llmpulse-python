# GeoAuditRun

One run of an audit. Null where an audit has no run yet (latest_run) or a comparison has no earlier run (from_run).

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

## Example

```python
from llmpulse.models.geo_audit_run import GeoAuditRun

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAuditRun from a JSON string
geo_audit_run_instance = GeoAuditRun.from_json(json)
# print the JSON string representation of the object
print(GeoAuditRun.to_json())

# convert the object into a dict
geo_audit_run_dict = geo_audit_run_instance.to_dict()
# create an instance of GeoAuditRun from a dict
geo_audit_run_from_dict = GeoAuditRun.from_dict(geo_audit_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


