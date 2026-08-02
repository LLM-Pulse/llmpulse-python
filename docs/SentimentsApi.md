# llmpulse.SentimentsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_sentiment_records**](SentimentsApi.md#list_sentiment_records) | **GET** /sentiments | List sentiment records


# **list_sentiment_records**
> list_sentiment_records(project_id, competitor_id=competitor_id, brand_only=brand_only, analysis=analysis, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, var_from=var_from, to=to, page=page, per_page=per_page)

List sentiment records

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
    competitor_id = 56 # int |  (optional)
    brand_only = True # bool |  (optional)
    analysis = 'analysis_example' # str |  (optional)
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = 56 # int |  (optional)
    country_code = 'country_code_example' # str | ISO country code (e.g. US, GB, DE) (optional)
    language_code = 'language_code_example' # str | ISO language code (e.g. en, es, de) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List sentiment records
        api_instance.list_sentiment_records(project_id, competitor_id=competitor_id, brand_only=brand_only, analysis=analysis, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, var_from=var_from, to=to, page=page, per_page=per_page)
    except Exception as e:
        print("Exception when calling SentimentsApi->list_sentiment_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **competitor_id** | **int**|  | [optional] 
 **brand_only** | **bool**|  | [optional] 
 **analysis** | **str**|  | [optional] 
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | **int**|  | [optional] 
 **country_code** | **str**| ISO country code (e.g. US, GB, DE) | [optional] 
 **language_code** | **str**| ISO language code (e.g. en, es, de) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**|  | [optional] 
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
**200** | Paginated sentiments |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

