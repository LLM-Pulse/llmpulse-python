# llmpulse.TechnicalGEOReportsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_technical_geo_reports**](TechnicalGEOReportsApi.md#create_technical_geo_reports) | **POST** /technical_geo_reports | Run technical GEO analysis
[**get_technical_geo_report**](TechnicalGEOReportsApi.md#get_technical_geo_report) | **GET** /technical_geo_reports/{id} | Get a technical GEO report
[**list_technical_geo_reports**](TechnicalGEOReportsApi.md#list_technical_geo_reports) | **GET** /technical_geo_reports | List technical GEO reports


# **create_technical_geo_reports**
> create_technical_geo_reports(create_technical_geo_reports_request)

Run technical GEO analysis

Launches the full technical GEO analysis bundle (crawlability, schema, content readiness, discoverability, site structure, robots.txt, agent readiness, llms.txt, AI visibility) for a URL + country. Each report runs in a background job. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.create_technical_geo_reports_request import CreateTechnicalGeoReportsRequest
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
    api_instance = llmpulse.TechnicalGEOReportsApi(api_client)
    create_technical_geo_reports_request = llmpulse.CreateTechnicalGeoReportsRequest() # CreateTechnicalGeoReportsRequest | 

    try:
        # Run technical GEO analysis
        api_instance.create_technical_geo_reports(create_technical_geo_reports_request)
    except Exception as e:
        print("Exception when calling TechnicalGEOReportsApi->create_technical_geo_reports: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_technical_geo_reports_request** | [**CreateTechnicalGeoReportsRequest**](CreateTechnicalGeoReportsRequest.md)|  | 

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
**201** | Created. app_urls maps each created report type to the link that opens that report in the app |  -  |
**403** | API key lacks write permission |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_technical_geo_report**
> get_technical_geo_report(project_id, report_type, id)

Get a technical GEO report

Returns the current status and the full result_data once the report is completed. While it is running, result_data is null and poll_after_seconds tells clients when to check again. Summaries carry output_language_code (the ISO 639-1 code an llms_txt report was requested in; null for an llms_txt report left on the website's own language in the app, and for every other report type); a completed llms_txt result_data also returns manually_edited_at, original_llms_txt_content and original_llms_full_txt_content (the generated files, set once the customer edited the files in the app) and metadata.output_language_code.

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
    api_instance = llmpulse.TechnicalGEOReportsApi(api_client)
    project_id = 56 # int | Project ID
    report_type = 'report_type_example' # str | 
    id = 56 # int | Report id returned by POST /technical_geo_reports or GET /technical_geo_reports

    try:
        # Get a technical GEO report
        api_instance.get_technical_geo_report(project_id, report_type, id)
    except Exception as e:
        print("Exception when calling TechnicalGEOReportsApi->get_technical_geo_report: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **report_type** | **str**|  | 
 **id** | **int**| Report id returned by POST /technical_geo_reports or GET /technical_geo_reports | 

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
**200** | Report status and completed result data, plus app_url, the link that opens the report in the app |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_technical_geo_reports**
> list_technical_geo_reports(project_id, report_type, status=status, batch_id=batch_id, page=page, per_page=per_page)

List technical GEO reports

Lists reports of one technical GEO type for a project, newest first. Use agent_readiness for the AI/Agent Readiness report.

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
    api_instance = llmpulse.TechnicalGEOReportsApi(api_client)
    project_id = 56 # int | Project ID
    report_type = 'report_type_example' # str | 
    status = 'status_example' # str | Optional status filter; valid values depend on report_type (optional)
    batch_id = 56 # int | Optional batch id returned when the report bundle was created (optional)
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)

    try:
        # List technical GEO reports
        api_instance.list_technical_geo_reports(project_id, report_type, status=status, batch_id=batch_id, page=page, per_page=per_page)
    except Exception as e:
        print("Exception when calling TechnicalGEOReportsApi->list_technical_geo_reports: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **report_type** | **str**|  | 
 **status** | **str**| Optional status filter; valid values depend on report_type | [optional] 
 **batch_id** | **int**| Optional batch id returned when the report bundle was created | [optional] 
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
**200** | Paginated technical GEO report summaries. Every summary carries app_url, the link that opens the report in the app |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

