# AdsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** |  | 
**page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** | Rows matching the filters across every page | 
**request_id** | **str** |  | 
**view** | **str** | advertisers or ads | 
**totals** | [**AdsTotals**](AdsTotals.md) |  | 
**data** | [**List[AdRow]**](AdRow.md) |  | 

## Example

```python
from llmpulse.models.ads_response import AdsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AdsResponse from a JSON string
ads_response_instance = AdsResponse.from_json(json)
# print the JSON string representation of the object
print(AdsResponse.to_json())

# convert the object into a dict
ads_response_dict = ads_response_instance.to_dict()
# create an instance of AdsResponse from a dict
ads_response_from_dict = AdsResponse.from_dict(ads_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


