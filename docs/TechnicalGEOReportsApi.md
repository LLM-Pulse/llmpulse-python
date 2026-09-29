# llmpulse.TechnicalGEOReportsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_technical_geo_reports**](TechnicalGEOReportsApi.md#create_technical_geo_reports) | **POST** /technical_geo_reports | Run technical GEO analysis
[**get_technical_geo_report**](TechnicalGEOReportsApi.md#get_technical_geo_report) | **GET** /technical_geo_reports/{id} | Get a technical GEO report
[**list_technical_geo_reports**](TechnicalGEOReportsApi.md#list_technical_geo_reports) | **GET** /technical_geo_reports | List technical GEO reports
[**revert_technical_geo_report_content**](TechnicalGEOReportsApi.md#revert_technical_geo_report_content) | **POST** /technical_geo_reports/{id}/revert_content | Revert llms.txt report content
[**update_technical_geo_report_content**](TechnicalGEOReportsApi.md#update_technical_geo_report_content) | **PATCH** /technical_geo_reports/{id}/content | Edit llms.txt report content


# **create_technical_geo_reports**
> create_technical_geo_reports(create_technical_geo_reports_request)

Run technical GEO analysis

Launches the full nine-report technical GEO analysis bundle for a URL + country. The bundle starts only when at least nine daily units remain. Each successfully created report uses one unit; a report that is not created uses none. Daily allocations vary by account. Each report runs in a background job. Requires a `read_write` scope API key.

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

Returns the current status and the full result_data once the report is completed. While it is running, result_data is null and poll_after_seconds tells clients when to check again. Summaries carry output_language_code (the ISO 639-1 code an llms_txt report was requested in; null for an llms_txt report written in the website's own language, requested as auto or chosen in the app, and for every other report type); a completed llms_txt result_data also returns content_version (send it back to PATCH /technical_geo_reports/{id}/content), manually_edited_at, original_llms_txt_content and original_llms_full_txt_content (the generated files, kept from the first manual edit in the app, the API or MCP) and metadata.output_language_code.

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

# **revert_technical_geo_report_content**
> LlmsTxtTechnicalGeoReport revert_technical_geo_report_content(id, technical_geo_report_content_revert_request)

Revert llms.txt report content

Discards every manual edit on the llms_txt report and restores the llms.txt and llms-full.txt files exactly as they were generated. Returns ERR_INVALID_PARAM when the report has no manual edits or report_type is not llms_txt. Requires a `read_write` scope API key and, for team members, create permission on GEO Optimization.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.llms_txt_technical_geo_report import LlmsTxtTechnicalGeoReport
from llmpulse.models.technical_geo_report_content_revert_request import TechnicalGeoReportContentRevertRequest
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
    id = 56 # int | Report id returned by POST /technical_geo_reports or GET /technical_geo_reports
    technical_geo_report_content_revert_request = llmpulse.TechnicalGeoReportContentRevertRequest() # TechnicalGeoReportContentRevertRequest | 

    try:
        # Revert llms.txt report content
        api_response = api_instance.revert_technical_geo_report_content(id, technical_geo_report_content_revert_request)
        print("The response of TechnicalGEOReportsApi->revert_technical_geo_report_content:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TechnicalGEOReportsApi->revert_technical_geo_report_content: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Report id returned by POST /technical_geo_reports or GET /technical_geo_reports | 
 **technical_geo_report_content_revert_request** | [**TechnicalGeoReportContentRevertRequest**](TechnicalGeoReportContentRevertRequest.md)|  | 

### Return type

[**LlmsTxtTechnicalGeoReport**](LlmsTxtTechnicalGeoReport.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The report with its generated files restored |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_technical_geo_report_content**
> TechnicalGeoReportContentUpdateResponse update_technical_geo_report_content(id, technical_geo_report_content_update_request)

Edit llms.txt report content

Replaces the llms.txt and llms-full.txt files of a completed llms_txt report in place, without generating them again. `edits` maps llms_txt and/or llms_full_txt to the full replacement text. `content_version` must equal result_data.content_version of the report as last read; when the report changed since, the edit is refused as stale and the message names the current version. A missing or stale content_version, a blank file, a file over 200,000 characters, a value that is not text, an unknown file key, an empty `edits` object, a report that has not completed or a report_type other than llms_txt is rejected with ERR_INVALID_PARAM and nothing is written. Files are stored with Unix line endings and one trailing newline. A file identical to the stored one is ignored, and the response lists the files that actually changed. The first edit keeps the generated files in original_llms_txt_content and original_llms_full_txt_content so POST /technical_geo_reports/{id}/revert_content can restore them; running the report again creates a new report without these edits. Requires a `read_write` scope API key and, for team members, create permission on GEO Optimization.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.technical_geo_report_content_update_request import TechnicalGeoReportContentUpdateRequest
from llmpulse.models.technical_geo_report_content_update_response import TechnicalGeoReportContentUpdateResponse
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
    id = 56 # int | Report id returned by POST /technical_geo_reports or GET /technical_geo_reports
    technical_geo_report_content_update_request = llmpulse.TechnicalGeoReportContentUpdateRequest() # TechnicalGeoReportContentUpdateRequest | 

    try:
        # Edit llms.txt report content
        api_response = api_instance.update_technical_geo_report_content(id, technical_geo_report_content_update_request)
        print("The response of TechnicalGEOReportsApi->update_technical_geo_report_content:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TechnicalGEOReportsApi->update_technical_geo_report_content: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Report id returned by POST /technical_geo_reports or GET /technical_geo_reports | 
 **technical_geo_report_content_update_request** | [**TechnicalGeoReportContentUpdateRequest**](TechnicalGeoReportContentUpdateRequest.md)|  | 

### Return type

[**TechnicalGeoReportContentUpdateResponse**](TechnicalGeoReportContentUpdateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The report with its current files, plus the files that changed |  -  |
**403** | API key lacks write permission |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

