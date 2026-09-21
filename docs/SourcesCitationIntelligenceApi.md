# llmpulse.SourcesCitationIntelligenceApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_cited_url_content**](SourcesCitationIntelligenceApi.md#get_cited_url_content) | **GET** /citation_intelligence/urls/{url_sha256}/content | Cited URL cached content
[**get_cited_url_detail**](SourcesCitationIntelligenceApi.md#get_cited_url_detail) | **GET** /citation_intelligence/urls/{url_sha256} | Cited URL detail
[**get_mentions_by_citing_domain**](SourcesCitationIntelligenceApi.md#get_mentions_by_citing_domain) | **GET** /citation_intelligence/mentions_by_domain | Mention share by citing domain
[**list_citation_groups**](SourcesCitationIntelligenceApi.md#list_citation_groups) | **GET** /citation_intelligence/groups | Grouped citation intelligence
[**list_cited_url_occurrences**](SourcesCitationIntelligenceApi.md#list_cited_url_occurrences) | **GET** /citation_intelligence/urls/{url_sha256}/occurrences | Cited URL occurrences
[**list_sources**](SourcesCitationIntelligenceApi.md#list_sources) | **GET** /dimensions/sources | List source URLs


# **get_cited_url_content**
> get_cited_url_content(project_id, url_sha256)

Cited URL cached content

Unavailable page content keeps the cited URL and citation metrics. Page metadata/content and unknown brand_mentioned/competitor_mentioned return null; content_gap_status is content_unavailable (or missing_page_cache). Mention arrays stay empty until usable content has completed analysis. status_code shows a saved successful response or observed 404/410; other crawl failures and error_message are hidden. last_crawled_at dates the saved copy. Domain/host crawled_urls_count counts usable copies; mention counts are null when no URL has completed analysis.

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
    api_instance = llmpulse.SourcesCitationIntelligenceApi(api_client)
    project_id = 56 # int | Project ID
    url_sha256 = 'url_sha256_example' # str | 64-character hex SHA-256 of the cited URL

    try:
        # Cited URL cached content
        api_instance.get_cited_url_content(project_id, url_sha256)
    except Exception as e:
        print("Exception when calling SourcesCitationIntelligenceApi->get_cited_url_content: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **url_sha256** | **str**| 64-character hex SHA-256 of the cited URL | 

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
**200** | Sanitized cached content + mention evidence |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cited_url_detail**
> get_cited_url_detail(project_id, url_sha256)

Cited URL detail

Unavailable page content keeps the cited URL and citation metrics. Page metadata/content and unknown brand_mentioned/competitor_mentioned return null; content_gap_status is content_unavailable (or missing_page_cache). Mention arrays stay empty until usable content has completed analysis. status_code shows a saved successful response or observed 404/410; other crawl failures and error_message are hidden. last_crawled_at dates the saved copy. Domain/host crawled_urls_count counts usable copies; mention counts are null when no URL has completed analysis.

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
    api_instance = llmpulse.SourcesCitationIntelligenceApi(api_client)
    project_id = 56 # int | Project ID
    url_sha256 = 'url_sha256_example' # str | 64-character hex SHA-256 of the cited URL

    try:
        # Cited URL detail
        api_instance.get_cited_url_detail(project_id, url_sha256)
    except Exception as e:
        print("Exception when calling SourcesCitationIntelligenceApi->get_cited_url_detail: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **url_sha256** | **str**| 64-character hex SHA-256 of the cited URL | 

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
**200** | URL-level intelligence |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_mentions_by_citing_domain**
> get_mentions_by_citing_domain(project_id, domains, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, brand_kind=brand_kind, var_from=var_from, to=to)

Mention share by citing domain

For the responses where each given source domain is cited, returns the share of those responses that mention the brand vs each competitor (brand + competitors sum to 100% per domain). Pass multiple domains to get the whole matrix in one call.

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
    api_instance = llmpulse.SourcesCitationIntelligenceApi(api_client)
    project_id = 56 # int | Project ID
    domains = ['domains_example'] # List[str] | Source domains to analyze, e.g. domains[]=gmac.com&domains[]=educaweb.com
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)

    try:
        # Mention share by citing domain
        api_instance.get_mentions_by_citing_domain(project_id, domains, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, brand_kind=brand_kind, var_from=var_from, to=to)
    except Exception as e:
        print("Exception when calling SourcesCitationIntelligenceApi->get_mentions_by_citing_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **domains** | [**List[str]**](str.md)| Source domains to analyze, e.g. domains[]&#x3D;gmac.com&amp;domains[]&#x3D;educaweb.com | 
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 

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
**200** | Mention share per citing domain |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_citation_groups**
> list_citation_groups(project_id, view=view, page=page, per_page=per_page, order=order, direction=direction, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, var_from=var_from, to=to, query=query, source_type=source_type, sentiment=sentiment, content_gap=content_gap)

Grouped citation intelligence

Grouped citation intelligence by url / domain / host with per-model breakdown, citation rate, and avg citation position. Counts and citation rate include visible citations and background source references. Average position ignores rows with position=0. Owned and competitor source matching honor the project's exact-subdomain setting. Filter vocabulary aligns with `source_type` returned by the API. Unavailable page content keeps the cited URL and citation metrics. Page metadata/content and unknown brand_mentioned/competitor_mentioned return null; content_gap_status is content_unavailable (or missing_page_cache). Mention arrays stay empty until usable content has completed analysis. status_code shows a saved successful response or observed 404/410; other crawl failures and error_message are hidden. last_crawled_at dates the saved copy. Domain/host crawled_urls_count counts usable copies; mention counts are null when no URL has completed analysis.

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
    api_instance = llmpulse.SourcesCitationIntelligenceApi(api_client)
    project_id = 56 # int | Project ID
    view = 'url' # str |  (optional) (default to 'url')
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    order = 'order_example' # str |  (optional)
    direction = 'direction_example' # str |  (optional)
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    query = 'query_example' # str |  (optional)
    source_type = 'source_type_example' # str |  (optional)
    sentiment = 'sentiment_example' # str |  (optional)
    content_gap = 'content_gap_example' # str |  (optional)

    try:
        # Grouped citation intelligence
        api_instance.list_citation_groups(project_id, view=view, page=page, per_page=per_page, order=order, direction=direction, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, var_from=var_from, to=to, query=query, source_type=source_type, sentiment=sentiment, content_gap=content_gap)
    except Exception as e:
        print("Exception when calling SourcesCitationIntelligenceApi->list_citation_groups: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **view** | **str**|  | [optional] [default to &#39;url&#39;]
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **order** | **str**|  | [optional] 
 **direction** | **str**|  | [optional] 
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **query** | **str**|  | [optional] 
 **source_type** | **str**|  | [optional] 
 **sentiment** | **str**|  | [optional] 
 **content_gap** | **str**|  | [optional] 

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
**200** | Grouped citation intelligence |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_cited_url_occurrences**
> list_cited_url_occurrences(project_id, url_sha256, page=page, per_page=per_page)

Cited URL occurrences

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
    api_instance = llmpulse.SourcesCitationIntelligenceApi(api_client)
    project_id = 56 # int | Project ID
    url_sha256 = 'url_sha256_example' # str | 64-character hex SHA-256 of the cited URL
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # Cited URL occurrences
        api_instance.list_cited_url_occurrences(project_id, url_sha256, page=page, per_page=per_page)
    except Exception as e:
        print("Exception when calling SourcesCitationIntelligenceApi->list_cited_url_occurrences: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **url_sha256** | **str**| 64-character hex SHA-256 of the cited URL | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]

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
**200** | Paginated occurrences |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_sources**
> list_sources(project_id, page=page, per_page=per_page, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, var_from=var_from, to=to, source_type=source_type, mention_filter=mention_filter, competitors=competitors, output=output)

List source URLs

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
    api_instance = llmpulse.SourcesCitationIntelligenceApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    source_type = 'source_type_example' # str | Filter by source ownership. Owned and competitor matching honor the project's exact-subdomain setting. (optional)
    mention_filter = 'mention_filter_example' # str | Filter by which brands are mentioned, as a two-axis matrix (your brand x competitors): mentions_you / not_mentions_you, mentions_competitor / not_mentions_competitor, and the four combined cells you_and_competitor, competitor_not_you (a rival wins and you are absent), you_not_competitor, no_brands (no tracked brand appears, i.e. open space). Combine with 'competitors' to narrow the competitor side to specific rivals; on a negative cell that reads 'none of these'. On /dimensions/sources it applies to the crawled content of each cited page instead of the answer text. The legacy value 'competitors_only' is still accepted as an alias of competitor_not_you. (optional)
    competitors = 'competitors_example' # str | Comma-separated competitor IDs (unknown IDs return ERR_INVALID_PARAM) (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List source URLs
        api_instance.list_sources(project_id, page=page, per_page=per_page, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, var_from=var_from, to=to, source_type=source_type, mention_filter=mention_filter, competitors=competitors, output=output)
    except Exception as e:
        print("Exception when calling SourcesCitationIntelligenceApi->list_sources: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **source_type** | **str**| Filter by source ownership. Owned and competitor matching honor the project&#39;s exact-subdomain setting. | [optional] 
 **mention_filter** | **str**| Filter by which brands are mentioned, as a two-axis matrix (your brand x competitors): mentions_you / not_mentions_you, mentions_competitor / not_mentions_competitor, and the four combined cells you_and_competitor, competitor_not_you (a rival wins and you are absent), you_not_competitor, no_brands (no tracked brand appears, i.e. open space). Combine with &#39;competitors&#39; to narrow the competitor side to specific rivals; on a negative cell that reads &#39;none of these&#39;. On /dimensions/sources it applies to the crawled content of each cited page instead of the answer text. The legacy value &#39;competitors_only&#39; is still accepted as an alias of competitor_not_you. | [optional] 
 **competitors** | **str**| Comma-separated competitor IDs (unknown IDs return ERR_INVALID_PARAM) | [optional] 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated sources |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

