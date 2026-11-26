# CitationSeries

The answers citing it under the same filters, by AI model and per period of the account tracking cadence

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**granularity** | **str** |  | 
**total** | **int** | Equal to total_responses | 
**by_model** | **Dict[str, int]** | Answers per AI model, keyed by model, largest first | 
**data** | [**List[AiModelPositionDistributionBrandBucketsInnerDataInner]**](AiModelPositionDistributionBrandBucketsInnerDataInner.md) | One point per period holding a filtered answer, oldest first; a zero means answers ran and none cited it | 

## Example

```python
from llmpulse.models.citation_series import CitationSeries

# TODO update the JSON string below
json = "{}"
# create an instance of CitationSeries from a JSON string
citation_series_instance = CitationSeries.from_json(json)
# print the JSON string representation of the object
print(CitationSeries.to_json())

# convert the object into a dict
citation_series_dict = citation_series_instance.to_dict()
# create an instance of CitationSeries from a dict
citation_series_from_dict = CitationSeries.from_dict(citation_series_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


