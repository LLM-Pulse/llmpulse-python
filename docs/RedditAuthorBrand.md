# RedditAuthorBrand


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_brand** | **bool** | True for your own brand | 
**id** | **int** | The competitor&#39;s id; null for your own brand | 
**name** | **str** |  | 
**count** | **int** | The author&#39;s cited posts whose content names the brand | 

## Example

```python
from llmpulse.models.reddit_author_brand import RedditAuthorBrand

# TODO update the JSON string below
json = "{}"
# create an instance of RedditAuthorBrand from a JSON string
reddit_author_brand_instance = RedditAuthorBrand.from_json(json)
# print the JSON string representation of the object
print(RedditAuthorBrand.to_json())

# convert the object into a dict
reddit_author_brand_dict = reddit_author_brand_instance.to_dict()
# create an instance of RedditAuthorBrand from a dict
reddit_author_brand_from_dict = RedditAuthorBrand.from_dict(reddit_author_brand_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


