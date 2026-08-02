# SummaryResponseAllOfPositionDistribution


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**position_1_count** | **int** |  | [optional] 
**position_2_count** | **int** |  | [optional] 
**position_3_plus_count** | **int** |  | [optional] 
**total_mentions** | **int** |  | [optional] 
**percentages** | **object** |  | [optional] 

## Example

```python
from llmpulse.models.summary_response_all_of_position_distribution import SummaryResponseAllOfPositionDistribution

# TODO update the JSON string below
json = "{}"
# create an instance of SummaryResponseAllOfPositionDistribution from a JSON string
summary_response_all_of_position_distribution_instance = SummaryResponseAllOfPositionDistribution.from_json(json)
# print the JSON string representation of the object
print(SummaryResponseAllOfPositionDistribution.to_json())

# convert the object into a dict
summary_response_all_of_position_distribution_dict = summary_response_all_of_position_distribution_instance.to_dict()
# create an instance of SummaryResponseAllOfPositionDistribution from a dict
summary_response_all_of_position_distribution_from_dict = SummaryResponseAllOfPositionDistribution.from_dict(summary_response_all_of_position_distribution_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


