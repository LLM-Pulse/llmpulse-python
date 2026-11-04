# OwnedMediaSummaryActivityPeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | Start date of the actual reporting period | 
**citations** | **int** |  | 
**yours** | **int** | Citations on owned profiles and content, null for provider&#x3D;overview | 
**other** | **int** | Citations not counted as yours, null for provider&#x3D;overview | 
**positive** | **int** | Citations whose AI answer sentiment is positive | [optional] 
**neutral** | **int** | Citations whose AI answer sentiment is neutral or mixed | [optional] 
**negative** | **int** | Citations whose AI answer sentiment is negative | [optional] 

## Example

```python
from llmpulse.models.owned_media_summary_activity_period import OwnedMediaSummaryActivityPeriod

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaSummaryActivityPeriod from a JSON string
owned_media_summary_activity_period_instance = OwnedMediaSummaryActivityPeriod.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaSummaryActivityPeriod.to_json())

# convert the object into a dict
owned_media_summary_activity_period_dict = owned_media_summary_activity_period_instance.to_dict()
# create an instance of OwnedMediaSummaryActivityPeriod from a dict
owned_media_summary_activity_period_from_dict = OwnedMediaSummaryActivityPeriod.from_dict(owned_media_summary_activity_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


