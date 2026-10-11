# PromptSummaryRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompt_id** | **int** |  | [optional] 
**prompt_text** | **str** |  | [optional] 
**model** | **str** | Only present when breakdown&#x3D;model | [optional] 
**responses** | **int** |  | [optional] 
**mentions** | **int** |  | [optional] 
**citations** | **int** |  | [optional] 
**visibility** | **float** |  | [optional] 
**mention_rate** | **float** |  | [optional] 
**citation_rate** | **float** |  | [optional] 
**avg_mention_position** | **float** |  | [optional] 
**avg_position** | **float** |  | [optional] 
**app_url** | **str** | Opens this prompt in the app. The link names its project, so it opens there for any user with access to that project | [optional] 
**country_code** | **str** | Country of the prompt, as in /dimensions/prompts | [optional] 
**language_code** | **str** | Language of the prompt, as in /dimensions/prompts | [optional] 
**prompt_type** | **str** | Search intent: informational, navigational, commercial or transactional. Null until the prompt is classified | [optional] 
**brand_kind** | **str** | Brand focus: brand, brand_other or non_brand. Null until the prompt is classified | [optional] 
**tags** | [**List[TagRef]**](TagRef.md) | Every tag the prompt belongs to | [optional] 
**sentiment_responses** | **int** | Responses in the window with a sentiment verdict for the brand, the base of the sentiment percentages (deduplicated like the sentiment timeseries) | [optional] 
**sentiment_very_positive** | **float** | Percentage (0-100) of sentiment_responses whose brand verdict is very positive; null when sentiment_responses is 0 | [optional] 
**sentiment_positive** | **float** | Percentage (0-100) of sentiment_responses whose brand verdict is positive; null when sentiment_responses is 0 | [optional] 
**sentiment_neutral** | **float** | Percentage (0-100) of sentiment_responses whose brand verdict is neutral; null when sentiment_responses is 0 | [optional] 
**sentiment_negative** | **float** | Percentage (0-100) of sentiment_responses whose brand verdict is negative; null when sentiment_responses is 0 | [optional] 
**sentiment_very_negative** | **float** | Percentage (0-100) of sentiment_responses whose brand verdict is very negative; null when sentiment_responses is 0 | [optional] 
**net_sentiment** | **float** | Positive minus negative percentages (-100 to 100), neutral counted in the base; null when sentiment_responses is 0 | [optional] 

## Example

```python
from llmpulse.models.prompt_summary_row import PromptSummaryRow

# TODO update the JSON string below
json = "{}"
# create an instance of PromptSummaryRow from a JSON string
prompt_summary_row_instance = PromptSummaryRow.from_json(json)
# print the JSON string representation of the object
print(PromptSummaryRow.to_json())

# convert the object into a dict
prompt_summary_row_dict = prompt_summary_row_instance.to_dict()
# create an instance of PromptSummaryRow from a dict
prompt_summary_row_from_dict = PromptSummaryRow.from_dict(prompt_summary_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


