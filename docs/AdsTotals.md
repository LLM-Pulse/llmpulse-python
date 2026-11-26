# AdsTotals


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ads** | **int** |  | 
**advertisers** | **int** |  | 
**your_ads** | **int** |  | 
**your_share** | **float** | your_ads over ads, 0-100 | 
**avg_position** | **float** |  | 
**executions_with_ads** | **int** |  | 

## Example

```python
from llmpulse.models.ads_totals import AdsTotals

# TODO update the JSON string below
json = "{}"
# create an instance of AdsTotals from a JSON string
ads_totals_instance = AdsTotals.from_json(json)
# print the JSON string representation of the object
print(AdsTotals.to_json())

# convert the object into a dict
ads_totals_dict = ads_totals_instance.to_dict()
# create an instance of AdsTotals from a dict
ads_totals_from_dict = AdsTotals.from_dict(ads_totals_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


