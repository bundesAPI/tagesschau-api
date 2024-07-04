# tagesschau.HomepageApi

All URIs are relative to *https://www.tagesschau.de*

Method | HTTP request | Description
------------- | ------------- | -------------
[**homepage**](HomepageApi.md#homepage) | **GET** /api2u/homepage/ | Ausgewählte aktuelle Nachrichten und Eilmeldungen


# **homepage**
> HomepageResponse homepage()

Ausgewählte aktuelle Nachrichten und Eilmeldungen

Ausgewählte aktuelle Nachrichten und Eilmeldungen, sowie regionale Nachrichten, die auf der Startseite der Tagesschau-App zu sehen sind.

### Example


```python
import time
from deutschland import tagesschau
from deutschland.tagesschau.api import homepage_api
from deutschland.tagesschau.model.homepage_response import HomepageResponse
from pprint import pprint
# Defining the host is optional and defaults to https://www.tagesschau.de
# See configuration.py for a list of all supported configuration parameters.
configuration = tagesschau.Configuration(
    host = "https://www.tagesschau.de"
)


# Enter a context with an instance of the API client
with tagesschau.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = homepage_api.HomepageApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Ausgewählte aktuelle Nachrichten und Eilmeldungen
        api_response = api_instance.homepage()
        pprint(api_response)
    except tagesschau.ApiException as e:
        print("Exception when calling HomepageApi->homepage: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**HomepageResponse**](HomepageResponse.md)

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

