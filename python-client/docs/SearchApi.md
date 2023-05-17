# tagesschau.SearchApi

All URIs are relative to *https://www.tagesschau.de*

Method | HTTP request | Description
------------- | ------------- | -------------
[**search**](SearchApi.md#search) | **GET** /api2/search/ | Suche


# **search**
> SearchResponse search()

Suche

Suche

### Example


```python
import time
from deutschland import tagesschau
from deutschland.tagesschau.api import search_api
from deutschland.tagesschau.model.search_response import SearchResponse
from pprint import pprint
# Defining the host is optional and defaults to https://www.tagesschau.de
# See configuration.py for a list of all supported configuration parameters.
configuration = tagesschau.Configuration(
    host = "https://www.tagesschau.de"
)


# Enter a context with an instance of the API client
with tagesschau.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = search_api.SearchApi(api_client)
    search_text = "Ukraine" # str | Suchtext (optional)
    page_size = 0 # int | Seite (optional)
    result_page = 2 # int | Suchergebnisse pro Seite (1-30) (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Suche
        api_response = api_instance.search(search_text=search_text, page_size=page_size, result_page=result_page)
        pprint(api_response)
    except tagesschau.ApiException as e:
        print("Exception when calling SearchApi->search: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search_text** | **str**| Suchtext | [optional]
 **page_size** | **int**| Seite | [optional]
 **result_page** | **int**| Suchergebnisse pro Seite (1-30) | [optional]

### Return type

[**SearchResponse**](SearchResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

