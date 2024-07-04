# tagesschau.ChannelsApi

All URIs are relative to *https://www.tagesschau.de*

Method | HTTP request | Description
------------- | ------------- | -------------
[**channels**](ChannelsApi.md#channels) | **GET** /api2u/channels/ | Aktuelle Kanäle


# **channels**
> ChannelsResponse channels()

Aktuelle Kanäle

Aktuelle Kanäle (im Livestream: tagesschau24, tagesschau in 100 Sekunden, tagesschau, tagesschau 20 Uhr, tagesthemen, nachtmagazin, Bericht aus Berlin, tagesschau vor 20 Jahren, tagesschau mit Gebärdensprache

### Example


```python
import time
from deutschland import tagesschau
from deutschland.tagesschau.api import channels_api
from deutschland.tagesschau.model.channels_response import ChannelsResponse
from pprint import pprint
# Defining the host is optional and defaults to https://www.tagesschau.de
# See configuration.py for a list of all supported configuration parameters.
configuration = tagesschau.Configuration(
    host = "https://www.tagesschau.de"
)


# Enter a context with an instance of the API client
with tagesschau.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = channels_api.ChannelsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Aktuelle Kanäle
        api_response = api_instance.channels()
        pprint(api_response)
    except tagesschau.ApiException as e:
        print("Exception when calling ChannelsApi->channels: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

[**ChannelsResponse**](ChannelsResponse.md)

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

