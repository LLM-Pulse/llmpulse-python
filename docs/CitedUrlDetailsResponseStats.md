# CitedUrlDetailsResponseStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_responses** | **int** | Answers citing the URL under the filters | 
**total_citations** | **int** |  | 
**citation_rate** | **float** | total_responses as a percentage (0-100) of citation_rate_denominator | 
**citation_rate_denominator** | **int** | Answers matching the filters | 
**avg_citation_position** | **float** | Null when no visible citation has a rank | 
**first_seen_at** | **datetime** | Null when no citation matches the filters | 
**last_seen_at** | **datetime** | Null when no citation matches the filters | 
**distinct_urls** | **int** | Spellings of the URL cited (tracking parameters, a trailing slash) | 
**source_types** | [**CitedUrlDetailsResponseStatsSourceTypes**](CitedUrlDetailsResponseStatsSourceTypes.md) |  | 
**models** | **Dict[str, int]** | Answers citing the URL per AI model, keyed by model | 

## Example

```python
from llmpulse.models.cited_url_details_response_stats import CitedUrlDetailsResponseStats

# TODO update the JSON string below
json = "{}"
# create an instance of CitedUrlDetailsResponseStats from a JSON string
cited_url_details_response_stats_instance = CitedUrlDetailsResponseStats.from_json(json)
# print the JSON string representation of the object
print(CitedUrlDetailsResponseStats.to_json())

# convert the object into a dict
cited_url_details_response_stats_dict = cited_url_details_response_stats_instance.to_dict()
# create an instance of CitedUrlDetailsResponseStats from a dict
cited_url_details_response_stats_from_dict = CitedUrlDetailsResponseStats.from_dict(cited_url_details_response_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


