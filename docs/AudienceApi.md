# openapi_client.AudienceApi

All URIs are relative to *https://api.redguy.ru*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1_audience_service_delete**](AudienceApi.md#v1_audience_service_delete) | **DELETE** /v1/audience/service | 
[**v1_audience_service_get**](AudienceApi.md#v1_audience_service_get) | **GET** /v1/audience/service | 
[**v1_audience_service_post**](AudienceApi.md#v1_audience_service_post) | **POST** /v1/audience/service | 
[**v1_audience_services_get**](AudienceApi.md#v1_audience_services_get) | **GET** /v1/audience/services | 
[**v1_audience_stats_get**](AudienceApi.md#v1_audience_stats_get) | **GET** /v1/audience/stats | 
[**v1_audience_user_get**](AudienceApi.md#v1_audience_user_get) | **GET** /v1/audience/user | 
[**v1_audience_user_post**](AudienceApi.md#v1_audience_user_post) | **POST** /v1/audience/user | 
[**v1_audience_users_get**](AudienceApi.md#v1_audience_users_get) | **GET** /v1/audience/users | 


# **v1_audience_service_delete**
> InlineResponse2001 v1_audience_service_delete()



Deletes audience service, requires audience permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import audience_api
from openapi_client.model.inline_response2001 import InlineResponse2001
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
    api_instance = audience_api.AudienceApi(api_client)
    id = 1 # int | Audience service id (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.v1_audience_service_delete(id=id)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling AudienceApi->v1_audience_service_delete: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Audience service id | [optional]

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_audience_service_get**
> InlineResponse2001 v1_audience_service_get()



Gets audience service, requires audience permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import audience_api
from openapi_client.model.inline_response2001 import InlineResponse2001
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
    api_instance = audience_api.AudienceApi(api_client)
    id = 1 # int | Audience service id (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.v1_audience_service_get(id=id)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling AudienceApi->v1_audience_service_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Audience service id | [optional]

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_audience_service_post**
> InlineResponse2001 v1_audience_service_post()



Creates audience service, requires audience permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import audience_api
from openapi_client.model.inline_response2001 import InlineResponse2001
from openapi_client.model.inline_object1 import InlineObject1
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
    api_instance = audience_api.AudienceApi(api_client)
    inline_object1 = InlineObject1(
        name="Имперский стражник",
    ) # InlineObject1 |  (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.v1_audience_service_post(inline_object1=inline_object1)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling AudienceApi->v1_audience_service_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inline_object1** | [**InlineObject1**](InlineObject1.md)|  | [optional]

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

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

# **v1_audience_services_get**
> InlineResponse2003 v1_audience_services_get()



Gets all audience services, requires audience permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import audience_api
from openapi_client.model.inline_response2003 import InlineResponse2003
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
    api_instance = audience_api.AudienceApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        api_response = api_instance.v1_audience_services_get()
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling AudienceApi->v1_audience_services_get: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_audience_stats_get**
> InlineResponse2002 v1_audience_stats_get()



Gets audience service and total users stats, requires audience permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import audience_api
from openapi_client.model.inline_response2002 import InlineResponse2002
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
    api_instance = audience_api.AudienceApi(api_client)
    id = 1 # int | Audience service id (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.v1_audience_stats_get(id=id)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling AudienceApi->v1_audience_stats_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Audience service id | [optional]

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_audience_user_get**
> InlineResponse2001 v1_audience_user_get()



Gets user, requires audience permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import audience_api
from openapi_client.model.inline_response2001 import InlineResponse2001
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
    api_instance = audience_api.AudienceApi(api_client)
    service_id = 1 # int | Audience service id (optional)
    user_id = "user_id_example" # str | User id (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.v1_audience_user_get(service_id=service_id, user_id=user_id)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling AudienceApi->v1_audience_user_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_id** | **int**| Audience service id | [optional]
 **user_id** | **str**| User id | [optional]

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_audience_user_post**
> InlineResponse2001Response v1_audience_user_post()



Posts user, requires audience permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import audience_api
from openapi_client.model.inline_object2 import InlineObject2
from openapi_client.model.inline_response2001_response import InlineResponse2001Response
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
    api_instance = audience_api.AudienceApi(api_client)
    inline_object2 = InlineObject2(
        code=1,
        comment="OK",
        response=V1AudienceUserResponse(
            service_id=1,
            user_id="1",
            data={},
        ),
    ) # InlineObject2 |  (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.v1_audience_user_post(inline_object2=inline_object2)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling AudienceApi->v1_audience_user_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inline_object2** | [**InlineObject2**](InlineObject2.md)|  | [optional]

### Return type

[**InlineResponse2001Response**](InlineResponse2001Response.md)

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

# **v1_audience_users_get**
> InlineResponse2003 v1_audience_users_get()



Gets all users, requires audience permission

### Example

* Bearer Authentication (bearerAuth):
```python
import time
import openapi_client
from openapi_client.api import audience_api
from openapi_client.model.inline_response2003 import InlineResponse2003
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
    api_instance = audience_api.AudienceApi(api_client)
    service_id = 1 # int | Audience service id (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        api_response = api_instance.v1_audience_users_get(service_id=service_id)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling AudienceApi->v1_audience_users_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_id** | **int**| Audience service id | [optional]

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

