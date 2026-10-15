# llmpulse.SentimentsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_sentiment_tags**](SentimentsApi.md#get_sentiment_tags) | **GET** /reports/sentiment/tags | Sentiment by tag (Growth plan or above)
[**get_sentiment_topics**](SentimentsApi.md#get_sentiment_topics) | **GET** /reports/sentiment/topics | Sentiment by topic (Growth plan or above)
[**list_sentiment_categories**](SentimentsApi.md#list_sentiment_categories) | **GET** /dimensions/sentiments | List sentiment categories (Growth plan or above)
[**list_sentiment_records**](SentimentsApi.md#list_sentiment_records) | **GET** /sentiments | List sentiment records (Growth plan or above)


# **get_sentiment_tags**
> SentimentTagsResponse get_sentiment_tags(project_id, range=range, var_from=var_from, to=to, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, brand_kind=brand_kind, analysis=analysis, topic=topic, query=query, brand=brand, sort=sort, sort_dir=sort_dir, page=page, per_page=per_page, output=output)

Sentiment by tag (Growth plan or above)

One row per tag of the project with at least one analyzed mention, with the positive (very positive included), neutral and negative counts, their shares on a 0-100 scale and the net sentiment score. A mention counts once for every tag its prompt carries, as on the Sentiment page. Same filters as GET /reports/sentiment/topics. Requires the Growth plan; lower tiers receive ERR_PLAN_REQUIRED.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.sentiment_tags_response import SentimentTagsResponse
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
    api_instance = llmpulse.SentimentsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back, today included (default 28, like the Sentiment page). Ignored when from or to is given. (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    model = 'model_example' # str | Filter by one AI model. It must be a model enabled for the API key's user: an unknown value, or a model the user has not enabled, returns 422 ERR_INVALID_PARAM with the valid values in the message. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    analysis = 'analysis_example' # str | One sentiment level or a comma-separated list: very_positive, positive, neutral, negative, very_negative (optional)
    topic = 'topic_example' # str | Only sentiments tagged with this topic (case-insensitive) (optional)
    query = 'query_example' # str | Only sentiments whose answer or prompt text contains this text (optional)
    brand = 'brand_example' # str | Whose sentiment to count. Empty or omitted for your own brand, all for every brand, or a competitor id (an unknown id returns ERR_INVALID_PARAM). (optional)
    sort = 'mentions' # str | Sort column: mentions, name (the topic or tag), positive, negative or neutral (their shares) or net_score. Ties sort by name. (optional) (default to 'mentions')
    sort_dir = 'desc' # str |  (optional) (default to 'desc')
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # Sentiment by tag (Growth plan or above)
        api_response = api_instance.get_sentiment_tags(project_id, range=range, var_from=var_from, to=to, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, brand_kind=brand_kind, analysis=analysis, topic=topic, query=query, brand=brand, sort=sort, sort_dir=sort_dir, page=page, per_page=per_page, output=output)
        print("The response of SentimentsApi->get_sentiment_tags:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SentimentsApi->get_sentiment_tags: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back, today included (default 28, like the Sentiment page). Ignored when from or to is given. | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **model** | **str**| Filter by one AI model. It must be a model enabled for the API key&#39;s user: an unknown value, or a model the user has not enabled, returns 422 ERR_INVALID_PARAM with the valid values in the message. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **analysis** | **str**| One sentiment level or a comma-separated list: very_positive, positive, neutral, negative, very_negative | [optional] 
 **topic** | **str**| Only sentiments tagged with this topic (case-insensitive) | [optional] 
 **query** | **str**| Only sentiments whose answer or prompt text contains this text | [optional] 
 **brand** | **str**| Whose sentiment to count. Empty or omitted for your own brand, all for every brand, or a competitor id (an unknown id returns ERR_INVALID_PARAM). | [optional] 
 **sort** | **str**| Sort column: mentions, name (the topic or tag), positive, negative or neutral (their shares) or net_score. Ties sort by name. | [optional] [default to &#39;mentions&#39;]
 **sort_dir** | **str**|  | [optional] [default to &#39;desc&#39;]
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**SentimentTagsResponse**](SentimentTagsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated tag rows |  -  |
**403** | Endpoint requires the Growth plan or above |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sentiment_topics**
> SentimentTopicsResponse get_sentiment_topics(project_id, range=range, var_from=var_from, to=to, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, brand_kind=brand_kind, analysis=analysis, topic=topic, query=query, brand=brand, sort=sort, sort_dir=sort_dir, page=page, per_page=per_page, output=output)

Sentiment by topic (Growth plan or above)

One row per topic AI answers associate with the brand (topics are matched case-insensitively), with its analyzed mentions, the positive (very positive included), neutral and negative counts, their shares on a 0-100 scale and the net sentiment score ((positive - negative) / mentions x 100). The same rows and filters as the Topics tab of the Sentiment page: the window defaults to the last 28 days, `brand` empty counts your own brand, `all` every brand and a competitor id that competitor. Requires the Growth plan; lower tiers receive ERR_PLAN_REQUIRED.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.sentiment_topics_response import SentimentTopicsResponse
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
    api_instance = llmpulse.SentimentsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back, today included (default 28, like the Sentiment page). Ignored when from or to is given. (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    model = 'model_example' # str | Filter by one AI model. It must be a model enabled for the API key's user: an unknown value, or a model the user has not enabled, returns 422 ERR_INVALID_PARAM with the valid values in the message. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    analysis = 'analysis_example' # str | One sentiment level or a comma-separated list: very_positive, positive, neutral, negative, very_negative (optional)
    topic = 'topic_example' # str | Only sentiments tagged with this topic (case-insensitive) (optional)
    query = 'query_example' # str | Only sentiments whose answer or prompt text contains this text (optional)
    brand = 'brand_example' # str | Whose sentiment to count. Empty or omitted for your own brand, all for every brand, or a competitor id (an unknown id returns ERR_INVALID_PARAM). (optional)
    sort = 'mentions' # str | Sort column: mentions, name (the topic or tag), positive, negative or neutral (their shares) or net_score. Ties sort by name. (optional) (default to 'mentions')
    sort_dir = 'desc' # str |  (optional) (default to 'desc')
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # Sentiment by topic (Growth plan or above)
        api_response = api_instance.get_sentiment_topics(project_id, range=range, var_from=var_from, to=to, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, brand_kind=brand_kind, analysis=analysis, topic=topic, query=query, brand=brand, sort=sort, sort_dir=sort_dir, page=page, per_page=per_page, output=output)
        print("The response of SentimentsApi->get_sentiment_topics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SentimentsApi->get_sentiment_topics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back, today included (default 28, like the Sentiment page). Ignored when from or to is given. | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **model** | **str**| Filter by one AI model. It must be a model enabled for the API key&#39;s user: an unknown value, or a model the user has not enabled, returns 422 ERR_INVALID_PARAM with the valid values in the message. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **analysis** | **str**| One sentiment level or a comma-separated list: very_positive, positive, neutral, negative, very_negative | [optional] 
 **topic** | **str**| Only sentiments tagged with this topic (case-insensitive) | [optional] 
 **query** | **str**| Only sentiments whose answer or prompt text contains this text | [optional] 
 **brand** | **str**| Whose sentiment to count. Empty or omitted for your own brand, all for every brand, or a competitor id (an unknown id returns ERR_INVALID_PARAM). | [optional] 
 **sort** | **str**| Sort column: mentions, name (the topic or tag), positive, negative or neutral (their shares) or net_score. Ties sort by name. | [optional] [default to &#39;mentions&#39;]
 **sort_dir** | **str**|  | [optional] [default to &#39;desc&#39;]
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**SentimentTopicsResponse**](SentimentTopicsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated topic rows |  -  |
**403** | Endpoint requires the Growth plan or above |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_sentiment_categories**
> list_sentiment_categories(project_id, output=output)

List sentiment categories (Growth plan or above)

Sentiment metric keys + labels + colors. For records, use /sentiments. Requires the Growth plan; lower tiers receive ERR_PLAN_REQUIRED.

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
    api_instance = llmpulse.SentimentsApi(api_client)
    project_id = 56 # int | Project ID
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List sentiment categories (Growth plan or above)
        api_instance.list_sentiment_categories(project_id, output=output)
    except Exception as e:
        print("Exception when calling SentimentsApi->list_sentiment_categories: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
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
**200** | Sentiment buckets |  -  |
**403** | Endpoint requires the Growth plan or above |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_sentiment_records**
> SentimentsResponse list_sentiment_records(project_id, competitor_id=competitor_id, brand_only=brand_only, analysis=analysis, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, var_from=var_from, to=to, page=page, per_page=per_page)

List sentiment records (Growth plan or above)

Requires the Growth plan; lower tiers receive ERR_PLAN_REQUIRED.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.sentiments_response import SentimentsResponse
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
    api_instance = llmpulse.SentimentsApi(api_client)
    project_id = 56 # int | Project ID
    competitor_id = 56 # int |  (optional)
    brand_only = True # bool |  (optional)
    analysis = 'analysis_example' # str | One sentiment level or a comma-separated list: very_positive, positive, neutral, negative, very_negative (optional)
    model = 'model_example' # str | Filter by one AI model. Here an unknown value, or a model the API key's user has not enabled, is ignored rather than rejected: the request succeeds and returns the records of every enabled model, as if model were omitted. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List sentiment records (Growth plan or above)
        api_response = api_instance.list_sentiment_records(project_id, competitor_id=competitor_id, brand_only=brand_only, analysis=analysis, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, var_from=var_from, to=to, page=page, per_page=per_page)
        print("The response of SentimentsApi->list_sentiment_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SentimentsApi->list_sentiment_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **competitor_id** | **int**|  | [optional] 
 **brand_only** | **bool**|  | [optional] 
 **analysis** | **str**| One sentiment level or a comma-separated list: very_positive, positive, neutral, negative, very_negative | [optional] 
 **model** | **str**| Filter by one AI model. Here an unknown value, or a model the API key&#39;s user has not enabled, is ignored rather than rejected: the request succeeds and returns the records of every enabled model, as if model were omitted. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]

### Return type

[**SentimentsResponse**](SentimentsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated sentiments |  -  |
**403** | Endpoint requires the Growth plan or above |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

