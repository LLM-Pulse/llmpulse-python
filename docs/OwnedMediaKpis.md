# OwnedMediaKpis


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** | Citations of the platform in the window, yours and everyone else&#39;s | [optional] 
**yours** | **int** | Citations of your own profiles and their content | [optional] 
**your_profile** | **int** | Citations of your profile or channel pages. Null for mobile_apps and overview | [optional] 
**your_content** | **int** | Citations of your posts or videos. Null for mobile_apps and overview | [optional] 
**share_pct** | **float** | yours as a percentage of total (0-100) | [optional] 

## Example

```python
from llmpulse.models.owned_media_kpis import OwnedMediaKpis

# TODO update the JSON string below
json = "{}"
# create an instance of OwnedMediaKpis from a JSON string
owned_media_kpis_instance = OwnedMediaKpis.from_json(json)
# print the JSON string representation of the object
print(OwnedMediaKpis.to_json())

# convert the object into a dict
owned_media_kpis_dict = owned_media_kpis_instance.to_dict()
# create an instance of OwnedMediaKpis from a dict
owned_media_kpis_from_dict = OwnedMediaKpis.from_dict(owned_media_kpis_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


