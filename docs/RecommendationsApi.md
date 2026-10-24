# llmpulse.RecommendationsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_recommendation**](RecommendationsApi.md#get_recommendation) | **GET** /recommendations/{id} | Get recommendation run with items
[**launch_recommendations**](RecommendationsApi.md#launch_recommendations) | **POST** /recommendations | Launch a recommendations generation
[**list_recommendations**](RecommendationsApi.md#list_recommendations) | **GET** /recommendations | List recommendation runs
[**update_recommendation_item**](RecommendationsApi.md#update_recommendation_item) | **PATCH** /recommendations/{id}/items/{item_id} | Complete, archive or restore a recommendation item


# **get_recommendation**
> get_recommendation(project_id, id, item_status=item_status, resolve_source_refs=resolve_source_refs)

Get recommendation run with items

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
    api_instance = llmpulse.RecommendationsApi(api_client)
    project_id = 56 # int | Project ID
    id = 56 # int | 
    item_status = 'item_status_example' # str |  (optional)
    resolve_source_refs = True # bool |  (optional) (default to True)

    try:
        # Get recommendation run with items
        api_instance.get_recommendation(project_id, id, item_status=item_status, resolve_source_refs=resolve_source_refs)
    except Exception as e:
        print("Exception when calling RecommendationsApi->get_recommendation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **int**|  | 
 **item_status** | **str**|  | [optional] 
 **resolve_source_refs** | **bool**|  | [optional] [default to True]

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
**200** | Recommendation detail with items |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **launch_recommendations**
> launch_recommendations(launch_recommendations_request)

Launch a recommendations generation

Launches a full-scope recommendations generation (async job, 1-3 minutes; poll GET /recommendations/{id} until status is completed). Consumes the project weekly recommendation-item budget: returns ERR_LIMIT_REACHED when it is exhausted or when a generation of the same type is already pending/processing. sentiment_reputation requires the Scale plan or above. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.launch_recommendations_request import LaunchRecommendationsRequest
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
    api_instance = llmpulse.RecommendationsApi(api_client)
    launch_recommendations_request = llmpulse.LaunchRecommendationsRequest() # LaunchRecommendationsRequest | 

    try:
        # Launch a recommendations generation
        api_instance.launch_recommendations(launch_recommendations_request)
    except Exception as e:
        print("Exception when calling RecommendationsApi->launch_recommendations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **launch_recommendations_request** | [**LaunchRecommendationsRequest**](LaunchRecommendationsRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Generation launched (status pending) |  -  |
**403** | API key lacks write permission |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_recommendations**
> RecommendationsResponse list_recommendations(project_id, recommendation_type=recommendation_type, status=status, page=page, per_page=per_page)

List recommendation runs

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.recommendations_response import RecommendationsResponse
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
    api_instance = llmpulse.RecommendationsApi(api_client)
    project_id = 56 # int | Project ID
    recommendation_type = 'recommendation_type_example' # str |  (optional)
    status = 'status_example' # str |  (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List recommendation runs
        api_response = api_instance.list_recommendations(project_id, recommendation_type=recommendation_type, status=status, page=page, per_page=per_page)
        print("The response of RecommendationsApi->list_recommendations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecommendationsApi->list_recommendations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **recommendation_type** | **str**|  | [optional] 
 **status** | **str**|  | [optional] 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]

### Return type

[**RecommendationsResponse**](RecommendationsResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated recommendations |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_recommendation_item**
> RecommendationItemUpdateResponse update_recommendation_item(id, item_id, update_recommendation_item_request)

Complete, archive or restore a recommendation item

Moves one item of a recommendation run between `active`, `completed` and `archived`, exactly like the complete, archive and restore buttons on the Recommendations page, and stamps `status_changed_at`. When archiving, an optional `reason` teaches later runs: `not_relevant` and `too_complex` steer the next recommendations away from similar ones, and on a PR & Citation Building item that targets a domain (`metadata.domain`), `competitor` or `not_relevant` stops that site from being suggested again. The reason is stored in `metadata.archive_reason` and dropped when the item leaves `archived`. A reason with another status, an unknown one, or `competitor` on an item without a domain returns `ERR_INVALID_PARAM`. Returns the item in the shape `GET /recommendations/{id}` lists items. Requires a `read_write` scope API key and, for team members, create permission on Recommendations (the permission the page uses for these buttons).

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.recommendation_item_update_response import RecommendationItemUpdateResponse
from llmpulse.models.update_recommendation_item_request import UpdateRecommendationItemRequest
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
    api_instance = llmpulse.RecommendationsApi(api_client)
    id = 56 # int | Recommendation run id
    item_id = 56 # int | Item id, from the items of GET /recommendations/{id}
    update_recommendation_item_request = llmpulse.UpdateRecommendationItemRequest() # UpdateRecommendationItemRequest | 

    try:
        # Complete, archive or restore a recommendation item
        api_response = api_instance.update_recommendation_item(id, item_id, update_recommendation_item_request)
        print("The response of RecommendationsApi->update_recommendation_item:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecommendationsApi->update_recommendation_item: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Recommendation run id | 
 **item_id** | **int**| Item id, from the items of GET /recommendations/{id} | 
 **update_recommendation_item_request** | [**UpdateRecommendationItemRequest**](UpdateRecommendationItemRequest.md)|  | 

### Return type

[**RecommendationItemUpdateResponse**](RecommendationItemUpdateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated item |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

