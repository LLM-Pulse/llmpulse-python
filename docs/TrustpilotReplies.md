# TrustpilotReplies

provider=trustpilot only. How the brand answers its Trustpilot reviews, on the profile of the project's own domain, among the reviews LLM Pulse holds for it (the newest ones from each monthly read, not every review on Trustpilot), whatever the date window. Every field is null until the profile has been read

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reviews_held** | **int** | Reviews held for the profile | [optional] 
**replied_count** | **int** | Reviews held that the brand replied to | [optional] 
**not_replied_count** | **int** | Reviews held that the brand has not replied to | [optional] 
**reply_rate_pct** | **float** | replied_count over reviews_held, on a 0-100 scale; null when no review is held | [optional] 
**median_reply_hours** | **float** | Median hours from publication to reply over the replied reviews held that carry both dates (a reply dated before its review is left out); null when there is none | [optional] 

## Example

```python
from llmpulse.models.trustpilot_replies import TrustpilotReplies

# TODO update the JSON string below
json = "{}"
# create an instance of TrustpilotReplies from a JSON string
trustpilot_replies_instance = TrustpilotReplies.from_json(json)
# print the JSON string representation of the object
print(TrustpilotReplies.to_json())

# convert the object into a dict
trustpilot_replies_dict = trustpilot_replies_instance.to_dict()
# create an instance of TrustpilotReplies from a dict
trustpilot_replies_from_dict = TrustpilotReplies.from_dict(trustpilot_replies_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


