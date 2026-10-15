# OwnedMediaSummaryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**provider** | **str** |  | [optional] 
**var_from** | **datetime** |  | [optional] 
**to** | **datetime** |  | [optional] 
**connected** | **bool** | Whether a profile is claimed on the platform (on overview, on any platform) | [optional] 
**kpis** | [**OwnedMediaKpis**](OwnedMediaKpis.md) |  | [optional] 
**previous** | [**OwnedMediaSummaryResponsePrevious**](OwnedMediaSummaryResponsePrevious.md) |  | [optional] 
**changes** | [**OwnedMediaKpiChanges**](OwnedMediaKpiChanges.md) |  | [optional] 
**weekly** | [**List[OwnedMediaWeek]**](OwnedMediaWeek.md) |  | [optional] 
**by_model** | [**List[OwnedMediaModelShare]**](OwnedMediaModelShare.md) | Null for provider&#x3D;overview | [optional] 
**by_country** | [**List[OwnedMediaCountryShare]**](OwnedMediaCountryShare.md) | Null for provider&#x3D;overview | [optional] 
**content_types** | [**List[OwnedMediaContentTypeShare]**](OwnedMediaContentTypeShare.md) | Social and YouTube providers only | [optional] 
**age_buckets** | [**List[OwnedMediaAgeBucketShare]**](OwnedMediaAgeBucketShare.md) | Social and YouTube providers only. Posts or videos without a known publication date are left out | [optional] 
**stores** | [**List[OwnedMediaStoreTotals]**](OwnedMediaStoreTotals.md) | provider&#x3D;mobile_apps only | [optional] 
**platforms** | [**List[OwnedMediaPlatformRollup]**](OwnedMediaPlatformRollup.md) | provider&#x3D;overview only, one row per platform the caller can read | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.owned_media_summary_response import OwnedMediaSummaryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaSummaryResponse from a JSON string
owned_media_summary_response_instance = OwnedMediaSummaryResponse.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaSummaryResponse.to_json())

# convert the object into a dict
owned_media_summary_response_dict = owned_media_summary_response_instance.to_dict()
# create an instance of OwnedMediaSummaryResponse from a dict
owned_media_summary_response_from_dict = OwnedMediaSummaryResponse.from_dict(owned_media_summary_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


