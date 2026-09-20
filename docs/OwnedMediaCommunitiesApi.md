# llmpulse.OwnedMediaCommunitiesApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_owned_media**](OwnedMediaCommunitiesApi.md#list_owned_media) | **GET** /dimensions/owned_media | List owned-media citations
[**list_reddit_citations**](OwnedMediaCommunitiesApi.md#list_reddit_citations) | **GET** /dimensions/reddit | List cited Reddit content


# **list_owned_media**
> list_owned_media(project_id, provider, page=page, per_page=per_page, view=view, store=store, owned=owned, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)

List owned-media citations

Which owned-media content AI answers cite, by platform. `provider` is required. Each row carries a `yours` flag so you can compare your own presence against everyone else cited on the same platform. view=own_citations returns the raw citations of the connected profile only and stays empty until a profile is connected. For Reddit use /dimensions/reddit. Requires the Growth plan or above.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.llmpulse.ai/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = llmpulse.Configuration(
    host = "https://api.llmpulse.ai/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: BearerAuth
configuration = llmpulse.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with llmpulse.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = llmpulse.OwnedMediaCommunitiesApi(api_client)
    project_id = 56 # int | Project ID
    provider = 'provider_example' # str | The platform to report on
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    view = 'view_example' # str | Row shape; the allowed set depends on provider (optional)
    store = 'google_play' # str | provider=mobile_apps only (optional) (default to 'google_play')
    owned = True # bool | Return only rows belonging to the account's own connected profile (optional)
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = llmpulse.GetTimeseriesCollectionIdParameter() # GetTimeseriesCollectionIdParameter | One collection/tag ID or a comma-separated list of IDs (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List owned-media citations
        api_instance.list_owned_media(project_id, provider, page=page, per_page=per_page, view=view, store=store, owned=owned, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)
    except Exception as e:
        print("Exception when calling OwnedMediaCommunitiesApi->list_owned_media: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **provider** | **str**| The platform to report on | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **view** | **str**| Row shape; the allowed set depends on provider | [optional] 
 **store** | **str**| provider&#x3D;mobile_apps only | [optional] [default to &#39;google_play&#39;]
 **owned** | **bool**| Return only rows belonging to the account&#39;s own connected profile | [optional] 
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | [**GetTimeseriesCollectionIdParameter**](.md)| One collection/tag ID or a comma-separated list of IDs | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated owned-media rows |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_reddit_citations**
> list_reddit_citations(project_id, page=page, per_page=per_page, view=view, subreddit=subreddit, author=author, status=status, owned=owned, brand=brand, order=order, direction=direction, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)

List cited Reddit content

Which Reddit content AI answers cite for your tracked prompts. view=subreddits (default) returns one row per subreddit with its citation count, unique authors and positive/negative sentiment split; view=authors returns one row per author; view=threads returns the individual cited threads with upvotes, comments, average position and dominant sentiment. Requires the Growth plan or above.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.llmpulse.ai/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = llmpulse.Configuration(
    host = "https://api.llmpulse.ai/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: BearerAuth
configuration = llmpulse.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with llmpulse.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = llmpulse.OwnedMediaCommunitiesApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    view = 'subreddits' # str |  (optional) (default to 'subreddits')
    subreddit = 'subreddit_example' # str | Filter to one subreddit (name without the r/ prefix) (optional)
    author = 'author_example' # str | Filter to one Reddit author (optional)
    status = 'status_example' # str | view=threads only (optional)
    owned = True # bool | Return only subreddits/authors the account has claimed as its own (optional)
    brand = 'brand_example' # str | Filter to citations whose scraped Reddit content mentions a brand: 'brand' for the tracked brand, or a competitor id. Reads the page content, not the AI answer. (optional)
    order = 'order_example' # str | Sort field; the allowed set depends on view (optional)
    direction = 'desc' # str |  (optional) (default to 'desc')
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = llmpulse.GetTimeseriesCollectionIdParameter() # GetTimeseriesCollectionIdParameter | One collection/tag ID or a comma-separated list of IDs (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List cited Reddit content
        api_instance.list_reddit_citations(project_id, page=page, per_page=per_page, view=view, subreddit=subreddit, author=author, status=status, owned=owned, brand=brand, order=order, direction=direction, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)
    except Exception as e:
        print("Exception when calling OwnedMediaCommunitiesApi->list_reddit_citations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **view** | **str**|  | [optional] [default to &#39;subreddits&#39;]
 **subreddit** | **str**| Filter to one subreddit (name without the r/ prefix) | [optional] 
 **author** | **str**| Filter to one Reddit author | [optional] 
 **status** | **str**| view&#x3D;threads only | [optional] 
 **owned** | **bool**| Return only subreddits/authors the account has claimed as its own | [optional] 
 **brand** | **str**| Filter to citations whose scraped Reddit content mentions a brand: &#39;brand&#39; for the tracked brand, or a competitor id. Reads the page content, not the AI answer. | [optional] 
 **order** | **str**| Sort field; the allowed set depends on view | [optional] 
 **direction** | **str**|  | [optional] [default to &#39;desc&#39;]
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | [**GetTimeseriesCollectionIdParameter**](.md)| One collection/tag ID or a comma-separated list of IDs | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated Reddit rows |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

