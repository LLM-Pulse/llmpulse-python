# llmpulse.ShoppingAdsApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_ads**](ShoppingAdsApi.md#list_ads) | **GET** /dimensions/ads | List AI ad placements
[**list_local_businesses**](ShoppingAdsApi.md#list_local_businesses) | **GET** /dimensions/local_businesses | List local businesses
[**list_shopping**](ShoppingAdsApi.md#list_shopping) | **GET** /dimensions/shopping | List shopping results


# **list_ads**
> list_ads(project_id, page=page, per_page=per_page, view=view, owned=owned, order=order, direction=direction, query=query, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)

List AI ad placements

Paid placements returned inside AI answers. view=advertisers (default) returns one row per advertising domain with its placement count, prompt reach and average and best position; view=ads returns the individual placements with title, snippet, position and the prompt that triggered them. Position 1 is the best slot, so a LOWER average position is better. Requires the Scale plan or above.

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
    api_instance = llmpulse.ShoppingAdsApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    view = 'advertisers' # str | Row shape: one per advertising domain, or one per placement (optional) (default to 'advertisers')
    owned = True # bool | Return only placements identified as the tracked brand's own (view=ads) (optional)
    order = 'order_example' # str | Sort field; the allowed set depends on view (optional)
    direction = 'direction_example' # str | Sort direction for view=advertisers. Defaults to desc, except avg_position and domain which default to asc. (optional)
    query = 'query_example' # str | Case-insensitive substring filter on the ad title, domain or snippet (optional)
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    prompt_type = 'prompt_type_example' # str | One prompt type or a comma-separated list: informational, navigational, commercial, transactional (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List AI ad placements
        api_instance.list_ads(project_id, page=page, per_page=per_page, view=view, owned=owned, order=order, direction=direction, query=query, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)
    except Exception as e:
        print("Exception when calling ShoppingAdsApi->list_ads: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **view** | **str**| Row shape: one per advertising domain, or one per placement | [optional] [default to &#39;advertisers&#39;]
 **owned** | **bool**| Return only placements identified as the tracked brand&#39;s own (view&#x3D;ads) | [optional] 
 **order** | **str**| Sort field; the allowed set depends on view | [optional] 
 **direction** | **str**| Sort direction for view&#x3D;advertisers. Defaults to desc, except avg_position and domain which default to asc. | [optional] 
 **query** | **str**| Case-insensitive substring filter on the ad title, domain or snippet | [optional] 
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **prompt_type** | **str**| One prompt type or a comma-separated list: informational, navigational, commercial, transactional | [optional] 
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
**200** | Paginated ad rows plus totals |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_local_businesses**
> LocalBusinessesResponse list_local_businesses(project_id, page=page, per_page=per_page, owned=owned, order=order, direction=direction, query=query, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)

List local businesses

Local businesses (shops, restaurants, services) listed inside AI answers, one row per business: its name at its address, so two locations of a chain are two rows. Each row carries its appearance count, the number of prompts that listed it, its average rating and average position in the list, its review count, and whether it is yours or a tracked competitor. Every response also carries a totals block matching the KPI cards in the app. Local business lists come from a subset of models and only for prompts with local intent. Available on every plan.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.local_businesses_response import LocalBusinessesResponse
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
    api_instance = llmpulse.ShoppingAdsApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    owned = True # bool | Return only listings identified as the tracked brand's own locations. The totals block stays account-wide. (optional)
    order = 'appearances' # str | Sort field (optional) (default to 'appearances')
    direction = 'desc' # str |  (optional) (default to 'desc')
    query = 'query_example' # str | Case-insensitive substring filter on the business name or address (optional)
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    prompt_type = 'prompt_type_example' # str | One prompt type or a comma-separated list: informational, navigational, commercial, transactional (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List local businesses
        api_response = api_instance.list_local_businesses(project_id, page=page, per_page=per_page, owned=owned, order=order, direction=direction, query=query, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)
        print("The response of ShoppingAdsApi->list_local_businesses:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShoppingAdsApi->list_local_businesses: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **owned** | **bool**| Return only listings identified as the tracked brand&#39;s own locations. The totals block stays account-wide. | [optional] 
 **order** | **str**| Sort field | [optional] [default to &#39;appearances&#39;]
 **direction** | **str**|  | [optional] [default to &#39;desc&#39;]
 **query** | **str**| Case-insensitive substring filter on the business name or address | [optional] 
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **prompt_type** | **str**| One prompt type or a comma-separated list: informational, navigational, commercial, transactional | [optional] 
 **brand_kind** | **str**| Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. | [optional] 
 **range** | **int**| Number of days to look back (alternative to from/to) | [optional] 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**| End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. | [optional] 
 **output** | **str**| Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. &#39;flat&#39; returns the same metadata plus &#39;columns&#39; and &#39;rows&#39;; &#39;csv&#39; returns those rows as text/csv. Errors are always returned as JSON. | [optional] 

### Return type

[**LocalBusinessesResponse**](LocalBusinessesResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated local business rows plus totals |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_shopping**
> list_shopping(project_id, page=page, per_page=per_page, view=view, owned=owned, order=order, direction=direction, query=query, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)

List shopping results

Product cards returned inside AI answers. view=products (default) returns one row per distinct product, merged across executions, with its appearance count, price range, rating and whether it is yours, plus a currency_count saying how many currencies it was priced in (above 1 means the row reports its highest-priced listing and min_price may be another currency); view=merchants returns one row per selling merchant, with a currency field naming the money its price range and average are expressed in (providers price each market in its own currency, so a merchant that sells in more than one reports the currency most of its prices use). Every response also carries a totals block matching the KPI cards in the app, whose avg_price is computed inside the single currency named by avg_price_currency. Requires the Scale plan or above.

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
    api_instance = llmpulse.ShoppingAdsApi(api_client)
    project_id = 56 # int | Project ID
    page = 1 # int |  (optional) (default to 1)
    per_page = 20 # int |  (optional) (default to 20)
    view = 'products' # str | Row shape: one per distinct product, or one per merchant (optional) (default to 'products')
    owned = True # bool | Return only products identified as the tracked brand's own. On view=merchants this narrows to the merchants selling those products; the totals block stays account-wide. (optional)
    order = 'order_example' # str | Sort field; the allowed set depends on view (optional)
    direction = 'desc' # str |  (optional) (default to 'desc')
    query = 'query_example' # str | Case-insensitive substring filter on the product title (optional)
    model = 'model_example' # str | Filter by AI model. Models the API key's user has not enabled are silently dropped. (optional)
    collection_id = '12,34' # str | One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. (optional)
    country_code = 'country_code_example' # str | One ISO country code or a comma-separated list (e.g. US,GB,DE) (optional)
    language_code = 'language_code_example' # str | One ISO language code or a comma-separated list (e.g. en,es,de) (optional)
    prompt = 56 # int | Filter by prompt ID (optional)
    prompt_type = 'prompt_type_example' # str | One prompt type or a comma-separated list: informational, navigational, commercial, transactional (optional)
    brand_kind = 'brand_kind_example' # str | Filter by brand kind: brand (own brand/products), brand_other (competitors/other brands), non_brand (generic, no brand named). For fair 1:1 brand-vs-competitor comparisons (visibility, share of voice), use non_brand: brand-focused prompts skew results toward the brand they name. The in-app Overview page applies non_brand by default. (optional)
    range = 56 # int | Number of days to look back (alternative to from/to) (optional)
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime | End of the window. A date-only value such as 2026-09-01 covers that whole day. Pass a full timestamp to end the window earlier. (optional)
    output = 'output_example' # str | Rectangular output for BI tools (Tableau, Excel, Sheets, ELT). Omit for the default nested JSON. 'flat' returns the same metadata plus 'columns' and 'rows'; 'csv' returns those rows as text/csv. Errors are always returned as JSON. (optional)

    try:
        # List shopping results
        api_instance.list_shopping(project_id, page=page, per_page=per_page, view=view, owned=owned, order=order, direction=direction, query=query, model=model, collection_id=collection_id, country_code=country_code, language_code=language_code, prompt=prompt, prompt_type=prompt_type, brand_kind=brand_kind, range=range, var_from=var_from, to=to, output=output)
    except Exception as e:
        print("Exception when calling ShoppingAdsApi->list_shopping: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **page** | **int**|  | [optional] [default to 1]
 **per_page** | **int**|  | [optional] [default to 20]
 **view** | **str**| Row shape: one per distinct product, or one per merchant | [optional] [default to &#39;products&#39;]
 **owned** | **bool**| Return only products identified as the tracked brand&#39;s own. On view&#x3D;merchants this narrows to the merchants selling those products; the totals block stays account-wide. | [optional] 
 **order** | **str**| Sort field; the allowed set depends on view | [optional] 
 **direction** | **str**|  | [optional] [default to &#39;desc&#39;]
 **query** | **str**| Case-insensitive substring filter on the product title | [optional] 
 **model** | **str**| Filter by AI model. Models the API key&#39;s user has not enabled are silently dropped. | [optional] 
 **collection_id** | **str**| One collection/tag ID or a comma-separated list of IDs. A query value is always a string on the wire, so it is typed as one: the previous integer-or-string union made generators emit a wrapper type they could not serialize. | [optional] 
 **country_code** | **str**| One ISO country code or a comma-separated list (e.g. US,GB,DE) | [optional] 
 **language_code** | **str**| One ISO language code or a comma-separated list (e.g. en,es,de) | [optional] 
 **prompt** | **int**| Filter by prompt ID | [optional] 
 **prompt_type** | **str**| One prompt type or a comma-separated list: informational, navigational, commercial, transactional | [optional] 
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
**200** | Paginated shopping rows plus totals |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

