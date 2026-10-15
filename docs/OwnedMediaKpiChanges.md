# OwnedMediaKpiChanges

Change against the previous period. Counts in percent, share_pct in percentage points; null when the previous period has nothing to compare with

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **float** |  | [optional] 
**yours** | **float** |  | [optional] 
**your_profile** | **float** |  | [optional] 
**your_content** | **float** |  | [optional] 
**share_pct** | **float** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_kpi_changes import OwnedMediaKpiChanges

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaKpiChanges from a JSON string
owned_media_kpi_changes_instance = OwnedMediaKpiChanges.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaKpiChanges.to_json())

# convert the object into a dict
owned_media_kpi_changes_dict = owned_media_kpi_changes_instance.to_dict()
# create an instance of OwnedMediaKpiChanges from a dict
owned_media_kpi_changes_from_dict = OwnedMediaKpiChanges.from_dict(owned_media_kpi_changes_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


