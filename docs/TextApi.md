# openapi_client.TextApi

All URIs are relative to *https://api.redguy.ru*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1_text_parse_post**](TextApi.md#v1_text_parse_post) | **POST** /v1/text/parse | 


# **v1_text_parse_post**
> InlineResponse200 v1_text_parse_post()



Parses text and returns a json object with found entities, requires text:parse permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import text_api
from openapi_client.model.inline_object import InlineObject
from openapi_client.model.inline_response200 import InlineResponse200
from pprint import pprint
# Defining the host is optional and defaults to https://api.redguy.ru
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.redguy.ru"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = openapi_client.Configuration(
    access_token = 'YOUR_BEARER_TOKEN'
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = text_api.TextApi(api_client)
    inline_object = InlineObject(
        text="5 утра",
        lang="ru_ru",
    ) # InlineObject |  (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.v1_text_parse_post(inline_object=inline_object)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling TextApi->v1_text_parse_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inline_object** | [**InlineObject**](InlineObject.md)|  | [optional]

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

