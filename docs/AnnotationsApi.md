# llmpulse.AnnotationsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_annotation**](AnnotationsApi.md#create_annotation) | **POST** /annotations | Create a timeline annotation
[**delete_annotation**](AnnotationsApi.md#delete_annotation) | **DELETE** /annotations/{id} | Delete a timeline annotation
[**list_annotations**](AnnotationsApi.md#list_annotations) | **GET** /annotations | List timeline annotations
[**update_annotation**](AnnotationsApi.md#update_annotation) | **PATCH** /annotations/{id} | Update a timeline annotation


# **create_annotation**
> AnnotationCreateResponse create_annotation(create_annotation_request)

Create a timeline annotation

Marks a date in the project timeseries with a title + description. Available on every plan. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.annotation_create_response import AnnotationCreateResponse
from llmpulse.models.create_annotation_request import CreateAnnotationRequest
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
    api_instance = llmpulse.AnnotationsApi(api_client)
    create_annotation_request = llmpulse.CreateAnnotationRequest() # CreateAnnotationRequest | 

    try:
        # Create a timeline annotation
        api_response = api_instance.create_annotation(create_annotation_request)
        print("The response of AnnotationsApi->create_annotation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnnotationsApi->create_annotation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_annotation_request** | [**CreateAnnotationRequest**](CreateAnnotationRequest.md)|  | 

### Return type

[**AnnotationCreateResponse**](AnnotationCreateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created |  -  |
**403** | API key lacks write permission |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_annotation**
> delete_annotation(project_id, id)

Delete a timeline annotation

Deletes an annotation. Same ownership rule as PATCH. Available on every plan and requires a `read_write` scope API key.

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
    api_instance = llmpulse.AnnotationsApi(api_client)
    project_id = 56 # int | Project ID
    id = 56 # int | 

    try:
        # Delete a timeline annotation
        api_instance.delete_annotation(project_id, id)
    except Exception as e:
        print("Exception when calling AnnotationsApi->delete_annotation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **id** | **int**|  | 

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
**200** | Deleted |  -  |
**403** | API key belongs to a team member whose permission matrix does not grant this feature |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_annotations**
> list_annotations(project_id, var_from=var_from, to=to, annotation_category_id=annotation_category_id, page=page, per_page=per_page)

List timeline annotations

Lists project timeline annotations, newest first. Rows can come from manual notes, project automations, GEO tests, or platform events. The origin field distinguishes them; editable says whether the requesting user may modify the row. Available on every plan.

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
    api_instance = llmpulse.AnnotationsApi(api_client)
    project_id = 56 # int | Project ID
    var_from = '2013-10-20' # date |  (optional)
    to = '2013-10-20' # date |  (optional)
    annotation_category_id = 56 # int |  (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List timeline annotations
        api_instance.list_annotations(project_id, var_from=var_from, to=to, annotation_category_id=annotation_category_id, page=page, per_page=per_page)
    except Exception as e:
        print("Exception when calling AnnotationsApi->list_annotations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **var_from** | **date**|  | [optional] 
 **to** | **date**|  | [optional] 
 **annotation_category_id** | **int**|  | [optional] 
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
**200** | Paginated annotations |  -  |
**403** | API key belongs to a team member whose permission matrix does not grant this feature |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_annotation**
> update_annotation(id, update_annotation_request)

Update a timeline annotation

Updates title, description, annotation_date, color and/or annotation_category_id. Only user-created annotations belonging to the requesting user can be updated (system annotations never). Available on every plan and requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.update_annotation_request import UpdateAnnotationRequest
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
    api_instance = llmpulse.AnnotationsApi(api_client)
    id = 56 # int | 
    update_annotation_request = llmpulse.UpdateAnnotationRequest() # UpdateAnnotationRequest | 

    try:
        # Update a timeline annotation
        api_instance.update_annotation(id, update_annotation_request)
    except Exception as e:
        print("Exception when calling AnnotationsApi->update_annotation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 
 **update_annotation_request** | [**UpdateAnnotationRequest**](UpdateAnnotationRequest.md)|  | 

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
**200** | Updated |  -  |
**403** | API key belongs to a team member whose permission matrix does not grant this feature |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

