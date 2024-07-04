# tagesschau.NewsApi

All URIs are relative to *https://www.tagesschau.de*

Method | HTTP request | Description
------------- | ------------- | -------------
[**news**](NewsApi.md#news) | **GET** /api2u/news/ | Aktuelle Nachrichten und Eilmeldungen


# **news**
> NewsResponse news()

Aktuelle Nachrichten und Eilmeldungen

Aktuelle Nachrichten und Eilmeldungen

### Example


```python
import time
from deutschland import tagesschau
from deutschland.tagesschau.api import news_api
from deutschland.tagesschau.model.news_response import NewsResponse
from pprint import pprint
# Defining the host is optional and defaults to https://www.tagesschau.de
# See configuration.py for a list of all supported configuration parameters.
configuration = tagesschau.Configuration(
    host = "https://www.tagesschau.de"
)


# Enter a context with an instance of the API client
with tagesschau.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = news_api.NewsApi(api_client)
    regions = 1 # int | Bundesland - 1=Baden-Württemberg, 2=Bayern, 3=Berlin, 4=Brandenburg, 5=Bremen, 6=Hamburg, 7=Hessen, 8=Mecklenburg-Vorpommern, 9=Niedersachsen, 10=Nordrhein-Westfalen, 11=Rheinland-Pfalz, 12=Saarland, 13=Sachsen, 14=Sachsen-Anhalt, 15=Schleswig-Holstein, 16=Thüringen. Mehrere Komma-getrennte Angaben möglich (z.B. regions=1,2). (optional)
    ressort = "ausland" # str | Ressort/Themengebiet (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Aktuelle Nachrichten und Eilmeldungen
        api_response = api_instance.news(regions=regions, ressort=ressort)
        pprint(api_response)
    except tagesschau.ApiException as e:
        print("Exception when calling NewsApi->news: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **regions** | **int**| Bundesland - 1&#x3D;Baden-Württemberg, 2&#x3D;Bayern, 3&#x3D;Berlin, 4&#x3D;Brandenburg, 5&#x3D;Bremen, 6&#x3D;Hamburg, 7&#x3D;Hessen, 8&#x3D;Mecklenburg-Vorpommern, 9&#x3D;Niedersachsen, 10&#x3D;Nordrhein-Westfalen, 11&#x3D;Rheinland-Pfalz, 12&#x3D;Saarland, 13&#x3D;Sachsen, 14&#x3D;Sachsen-Anhalt, 15&#x3D;Schleswig-Holstein, 16&#x3D;Thüringen. Mehrere Komma-getrennte Angaben möglich (z.B. regions&#x3D;1,2). | [optional]
 **ressort** | **str**| Ressort/Themengebiet | [optional]

### Return type

[**NewsResponse**](NewsResponse.md)

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

