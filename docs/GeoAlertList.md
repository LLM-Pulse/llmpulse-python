# GeoAlertList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**data** | [**List[GeoAlert]**](GeoAlert.md) |  | [optional] 
**request_id** | **str** |  | [optional] 

## Example

```python
from llmpulse.models.geo_alert_list import GeoAlertList

# TODO update the JSON string below
json = "{}"
# create an instance of GeoAlertList from a JSON string
geo_alert_list_instance = GeoAlertList.from_json(json)
# print the JSON string representation of the object
print(GeoAlertList.to_json())

# convert the object into a dict
geo_alert_list_dict = geo_alert_list_instance.to_dict()
# create an instance of GeoAlertList from a dict
geo_alert_list_from_dict = GeoAlertList.from_dict(geo_alert_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


