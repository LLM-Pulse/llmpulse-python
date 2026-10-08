# llmpulse.SentimentsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_sentiment_categories**](SentimentsApi.md#list_sentiment_categories) | **GET** /dimensions/sentiments | List sentiment categories (Growth plan or above)
[**list_sentiment_records**](SentimentsApi.md#list_sentiment_records) | **GET** /sentiments | List sentiment records (Growth plan or above)


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
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
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
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
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

