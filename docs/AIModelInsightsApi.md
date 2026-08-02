# llmpulse.AIModelInsightsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ai_model_insights_summary**](AIModelInsightsApi.md#get_ai_model_insights_summary) | **GET** /reports/ai_model_insights/summary | AI Model Insights summary
[**get_ai_model_position_distribution**](AIModelInsightsApi.md#get_ai_model_position_distribution) | **GET** /reports/ai_model_insights/position_distribution | Position distribution comparison
[**get_ai_overview_results**](AIModelInsightsApi.md#get_ai_overview_results) | **GET** /reports/ai_model_insights/ai_overview_results | Google AI Overview result availability


# **get_ai_model_insights_summary**
> get_ai_model_insights_summary(project_id, range=range, var_from=var_from, to=to, granularity=granularity, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt_type=prompt_type, brand_kind=brand_kind, competitors=competitors)

AI Model Insights summary

Per-model mentions, citations, brand net sentiment with raw counts, weighted visibility totals/shares, plus actor matrices. All actor entries use the standard shape `{ type, id, competitor_id, name, domain }` with bare (scheme-less) domains.

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
    api_instance = llmpulse.AIModelInsightsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    granularity = 'granularity_example' # str |  (optional)
    collection_id = 56 # int |  (optional)
    country_code = 'country_code_example' # str | ISO country code (e.g. US, GB, DE) (optional)
    language_code = 'language_code_example' # str | ISO language code (e.g. en, es, de) (optional)
    prompt_type = 'prompt_type_example' # str | Filter by prompt type (search intent) (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    competitors = 'competitors_example' # str | Comma-separated competitor IDs (unknown IDs return ERR_INVALID_PARAM) (optional)

    try:
        # AI Model Insights summary
        api_instance.get_ai_model_insights_summary(project_id, range=range, var_from=var_from, to=to, granularity=granularity, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt_type=prompt_type, brand_kind=brand_kind, competitors=competitors)
    except Exception as e:
        print("Exception when calling AIModelInsightsApi->get_ai_model_insights_summary: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**|  | [optional] 
 **granularity** | **str**|  | [optional] 
 **collection_id** | **int**|  | [optional] 
 **country_code** | **str**| ISO country code (e.g. US, GB, DE) | [optional] 
 **language_code** | **str**| ISO language code (e.g. en, es, de) | [optional] 
 **prompt_type** | **str**| Filter by prompt type (search intent) | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **competitors** | **str**| Comma-separated competitor IDs (unknown IDs return ERR_INVALID_PARAM) | [optional] 

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
**200** | Summary |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ai_model_position_distribution**
> get_ai_model_position_distribution(project_id, range=range, var_from=var_from, to=to, granularity=granularity, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt_type=prompt_type, brand_kind=brand_kind, model=model, brand1=brand1, brand2=brand2)

Position distribution comparison

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
    api_instance = llmpulse.AIModelInsightsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    granularity = 'granularity_example' # str |  (optional)
    collection_id = 56 # int |  (optional)
    country_code = 'country_code_example' # str | ISO country code (e.g. US, GB, DE) (optional)
    language_code = 'language_code_example' # str | ISO language code (e.g. en, es, de) (optional)
    prompt_type = 'prompt_type_example' # str | Filter by prompt type (search intent) (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    brand1 = 56 # int | Competitor ID for the first comparison brand (omit to compare project brand) (optional)
    brand2 = 56 # int |  (optional)

    try:
        # Position distribution comparison
        api_instance.get_ai_model_position_distribution(project_id, range=range, var_from=var_from, to=to, granularity=granularity, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt_type=prompt_type, brand_kind=brand_kind, model=model, brand1=brand1, brand2=brand2)
    except Exception as e:
        print("Exception when calling AIModelInsightsApi->get_ai_model_position_distribution: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**|  | [optional] 
 **granularity** | **str**|  | [optional] 
 **collection_id** | **int**|  | [optional] 
 **country_code** | **str**| ISO country code (e.g. US, GB, DE) | [optional] 
 **language_code** | **str**| ISO language code (e.g. en, es, de) | [optional] 
 **prompt_type** | **str**| Filter by prompt type (search intent) | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **brand1** | **int**| Competitor ID for the first comparison brand (omit to compare project brand) | [optional] 
 **brand2** | **int**|  | [optional] 

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
**200** | Bucketed position totals + chart-ready series |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ai_overview_results**
> get_ai_overview_results(project_id, range=range, var_from=var_from, to=to, granularity=granularity, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt_type=prompt_type, brand_kind=brand_kind, page=page, per_page=per_page)

Google AI Overview result availability

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
    api_instance = llmpulse.AIModelInsightsApi(api_client)
    project_id = 56 # int | Project ID
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    granularity = 'granularity_example' # str |  (optional)
    collection_id = 56 # int |  (optional)
    country_code = 'country_code_example' # str | ISO country code (e.g. US, GB, DE) (optional)
    language_code = 'language_code_example' # str | ISO language code (e.g. en, es, de) (optional)
    prompt_type = 'prompt_type_example' # str | Filter by prompt type (search intent) (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # Google AI Overview result availability
        api_instance.get_ai_overview_results(project_id, range=range, var_from=var_from, to=to, granularity=granularity, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt_type=prompt_type, brand_kind=brand_kind, page=page, per_page=per_page)
    except Exception as e:
        print("Exception when calling AIModelInsightsApi->get_ai_overview_results: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**|  | [optional] 
 **granularity** | **str**|  | [optional] 
 **collection_id** | **int**|  | [optional] 
 **country_code** | **str**| ISO country code (e.g. US, GB, DE) | [optional] 
 **language_code** | **str**| ISO language code (e.g. en, es, de) | [optional] 
 **prompt_type** | **str**| Filter by prompt type (search intent) | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]

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
**200** | AI Overview result-availability data + per-prompt table |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

