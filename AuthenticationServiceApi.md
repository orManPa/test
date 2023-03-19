# PyramidAnalytics.Api3.Api.AuthenticationServiceApi

All URIs are relative to *http://Domain*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AuthenticateUser**](AuthenticationServiceApi.md#authenticateuser) | **POST** /API3/auth/authenticateUser | Generates an access authentication token for the given user to use the API functions or login to the application. |
| [**AuthenticateUserByToken**](AuthenticationServiceApi.md#authenticateuserbytoken) | **POST** /API3/auth/authenticateUserByToken | Generates an access authentication token for a given user without their password, using an administrative token to authorize login to the application instead. |
| [**AuthenticateUserEmbed**](AuthenticationServiceApi.md#authenticateuserembed) | **POST** /API3/auth/authenticateUserEmbed | Generates an access authentication token for the given user to use the embedded content functionality. |
| [**AuthenticateUserEmbedByToken**](AuthenticationServiceApi.md#authenticateuserembedbytoken) | **POST** /API3/auth/authenticateUserEmbedByToken | Generates an access authentication token for embedding content, for a given user without their password, using an administrative token. |
| [**AuthenticateUserEmbedOPENID**](AuthenticationServiceApi.md#authenticateuserembedopenid) | **POST** /API3/auth/authenticateUserEmbedOPENID | Generates a Pyramid access authentication token for embedding using OpenID parameter map |
| [**AuthenticateUserEmbedSAML**](AuthenticationServiceApi.md#authenticateuserembedsaml) | **POST** /API3/auth/authenticateUserEmbedSAML | Generates a Pyramid access authentication token for embedding using SAML authentication tokens |
| [**AuthenticateUserEmbedWindows**](AuthenticationServiceApi.md#authenticateuserembedwindows) | **POST** /API3/auth/authenticateUserEmbedWindows | Generates a Pyramid access authentication token for embedding using Windows Authentication tokens |
| [**AuthenticateUserOPENID**](AuthenticationServiceApi.md#authenticateuseropenid) | **POST** /API3/auth/authenticateUserOPENID | Generates a Pyramid access authentication token using OpenID authentication parameter map |
| [**AuthenticateUserOPENIDAlt**](AuthenticationServiceApi.md#authenticateuseropenidalt) | **POST** /API3/auth/authenticateUserOPENIDAlt | Generates a Pyramid access authentication token using OpenID authentication parameter map and custom data |
| [**AuthenticateUserSAML**](AuthenticationServiceApi.md#authenticateusersaml) | **POST** /API3/auth/authenticateUserSAML | Generates a Pyramid access authentication token using SAML authentication tokens |
| [**AuthenticateUserSAMLAlt**](AuthenticationServiceApi.md#authenticateusersamlalt) | **POST** /API3/auth/authenticateUserSAMLAlt | Generates a Pyramid access authentication token using SAML authentication tokens and custom data |
| [**AuthenticateUserWindows**](AuthenticationServiceApi.md#authenticateuserwindows) | **POST** /API3/auth/authenticateUserWindows | Generates a Pyramid access authentication token using windows authentication tokens |

<a name="authenticateuser"></a>
# **AuthenticateUser**
> string AuthenticateUser (UserCredentials userCredentials)

Generates an access authentication token for the given user to use the API functions or login to the application.

The security token is a string that needs to be embedded in every API call to ensure the API calls are authorized. If saved as a cookie in a web browser, it can be used (for the authenticated user) to auto-login into the application.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var userCredentials = new UserCredentials(); // UserCredentials | 

            try
            {
                // Generates an access authentication token for the given user to use the API functions or login to the application.
                string result = apiInstance.AuthenticateUser(userCredentials);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUser: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates an access authentication token for the given user to use the API functions or login to the application.
    ApiResponse<string> response = apiInstance.AuthenticateUserWithHttpInfo(userCredentials);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userCredentials** | [**UserCredentials**](UserCredentials.md) |  |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuserbytoken"></a>
# **AuthenticateUserByToken**
> string AuthenticateUserByToken (UserTokenCredentials userTokenCredentials)

Generates an access authentication token for a given user without their password, using an administrative token to authorize login to the application instead.

The security token is an authentication token that needs to be first generated by an administrative user with full credentials first.When saved as a cookie in a web browser, it can then be used to auto-login the user into the application.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserByTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var userTokenCredentials = new UserTokenCredentials(); // UserTokenCredentials | 

            try
            {
                // Generates an access authentication token for a given user without their password, using an administrative token to authorize login to the application instead.
                string result = apiInstance.AuthenticateUserByToken(userTokenCredentials);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserByToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserByTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates an access authentication token for a given user without their password, using an administrative token to authorize login to the application instead.
    ApiResponse<string> response = apiInstance.AuthenticateUserByTokenWithHttpInfo(userTokenCredentials);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserByTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userTokenCredentials** | [**UserTokenCredentials**](UserTokenCredentials.md) |  |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuserembed"></a>
# **AuthenticateUserEmbed**
> string AuthenticateUserEmbed (UserCredentials userCredentials)

Generates an access authentication token for the given user to use the embedded content functionality.

The security token is a string that needs to be added to a cookie on the third party host page for any embedded content to ensure the access is authorized.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserEmbedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var userCredentials = new UserCredentials(); // UserCredentials | 

            try
            {
                // Generates an access authentication token for the given user to use the embedded content functionality.
                string result = apiInstance.AuthenticateUserEmbed(userCredentials);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserEmbedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates an access authentication token for the given user to use the embedded content functionality.
    ApiResponse<string> response = apiInstance.AuthenticateUserEmbedWithHttpInfo(userCredentials);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userCredentials** | [**UserCredentials**](UserCredentials.md) |  |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuserembedbytoken"></a>
# **AuthenticateUserEmbedByToken**
> string AuthenticateUserEmbedByToken (UserTokenCredentials userTokenCredentials)

Generates an access authentication token for embedding content, for a given user without their password, using an administrative token.

The security token is an authentication ticket that needs to be first generated by an administrative user with full credentials.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserEmbedByTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var userTokenCredentials = new UserTokenCredentials(); // UserTokenCredentials | 

            try
            {
                // Generates an access authentication token for embedding content, for a given user without their password, using an administrative token.
                string result = apiInstance.AuthenticateUserEmbedByToken(userTokenCredentials);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedByToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserEmbedByTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates an access authentication token for embedding content, for a given user without their password, using an administrative token.
    ApiResponse<string> response = apiInstance.AuthenticateUserEmbedByTokenWithHttpInfo(userTokenCredentials);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedByTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userTokenCredentials** | [**UserTokenCredentials**](UserTokenCredentials.md) |  |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuserembedopenid"></a>
# **AuthenticateUserEmbedOPENID**
> string AuthenticateUserEmbedOPENID (UserOpenIdCredentials userOpenIdCredentials)

Generates a Pyramid access authentication token for embedding using OpenID parameter map

The security token is a string that needs to be added to a cookie on the third party host page for any embedded content to ensure the access is authorized. The assumption is that the user has already authenticated via OPENID in the hosting application before attempting to authenticate into Pyramid.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserEmbedOPENIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var userOpenIdCredentials = new UserOpenIdCredentials(); // UserOpenIdCredentials | 

            try
            {
                // Generates a Pyramid access authentication token for embedding using OpenID parameter map
                string result = apiInstance.AuthenticateUserEmbedOPENID(userOpenIdCredentials);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedOPENID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserEmbedOPENIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates a Pyramid access authentication token for embedding using OpenID parameter map
    ApiResponse<string> response = apiInstance.AuthenticateUserEmbedOPENIDWithHttpInfo(userOpenIdCredentials);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedOPENIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userOpenIdCredentials** | [**UserOpenIdCredentials**](UserOpenIdCredentials.md) |  |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuserembedsaml"></a>
# **AuthenticateUserEmbedSAML**
> string AuthenticateUserEmbedSAML (UserSamlCredentials userOpenIdCredentials)

Generates a Pyramid access authentication token for embedding using SAML authentication tokens

The security token is a string that needs to be added to a cookie on the third party host page for any embedded content to ensure the access is authorized. The assumption is that the user has already authenticated via SAML in the hosting application before attempting to authenticate into Pyramid.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserEmbedSAMLExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var userOpenIdCredentials = new UserSamlCredentials(); // UserSamlCredentials | 

            try
            {
                // Generates a Pyramid access authentication token for embedding using SAML authentication tokens
                string result = apiInstance.AuthenticateUserEmbedSAML(userOpenIdCredentials);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedSAML: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserEmbedSAMLWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates a Pyramid access authentication token for embedding using SAML authentication tokens
    ApiResponse<string> response = apiInstance.AuthenticateUserEmbedSAMLWithHttpInfo(userOpenIdCredentials);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedSAMLWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userOpenIdCredentials** | [**UserSamlCredentials**](UserSamlCredentials.md) |  |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuserembedwindows"></a>
# **AuthenticateUserEmbedWindows**
> string AuthenticateUserEmbedWindows (string domain)

Generates a Pyramid access authentication token for embedding using Windows Authentication tokens

The security token is a string that needs to be added to a cookie on the third party host page for any embedded content to ensure the access is authorized. The web browser must support Windows Authentication and the authentication METHOD must be set to 'Windows Authentication' in Pyramid.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserEmbedWindowsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var domain = "domain_example";  // string | The URL web domain - needed only for embedded authentication.

            try
            {
                // Generates a Pyramid access authentication token for embedding using Windows Authentication tokens
                string result = apiInstance.AuthenticateUserEmbedWindows(domain);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedWindows: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserEmbedWindowsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates a Pyramid access authentication token for embedding using Windows Authentication tokens
    ApiResponse<string> response = apiInstance.AuthenticateUserEmbedWindowsWithHttpInfo(domain);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserEmbedWindowsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **domain** | **string** | The URL web domain - needed only for embedded authentication. |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuseropenid"></a>
# **AuthenticateUserOPENID**
> string AuthenticateUserOPENID (string parameterMap)

Generates a Pyramid access authentication token using OpenID authentication parameter map

The security token is a string that needs to be embedded in every API call to ensure the API calls are authorized. If saved as a cookie in a web browser, it can be used (for the authenticated user) to auto-login into the application. The assumption is that the user has already authenticated via OpenID before attempting to authenticate into Pyramid.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserOPENIDExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var parameterMap = "parameterMap_example";  // string | The OpenID parameter map serialized to String representation

            try
            {
                // Generates a Pyramid access authentication token using OpenID authentication parameter map
                string result = apiInstance.AuthenticateUserOPENID(parameterMap);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserOPENID: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserOPENIDWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates a Pyramid access authentication token using OpenID authentication parameter map
    ApiResponse<string> response = apiInstance.AuthenticateUserOPENIDWithHttpInfo(parameterMap);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserOPENIDWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **parameterMap** | **string** | The OpenID parameter map serialized to String representation |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuseropenidalt"></a>
# **AuthenticateUserOPENIDAlt**
> string AuthenticateUserOPENIDAlt (UserOpenIdCredentials userOpenIdCredentials)

Generates a Pyramid access authentication token using OpenID authentication parameter map and custom data

The security token is a string that needs to be embedded in every API call to ensure the API calls are authorized. If saved as a cookie in a web browser, it can be used (for the authenticated user) to auto-login into the application. The assumption is that the user has already authenticated via OpenID before attempting to authenticate into Pyramid.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserOPENIDAltExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var userOpenIdCredentials = new UserOpenIdCredentials(); // UserOpenIdCredentials | 

            try
            {
                // Generates a Pyramid access authentication token using OpenID authentication parameter map and custom data
                string result = apiInstance.AuthenticateUserOPENIDAlt(userOpenIdCredentials);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserOPENIDAlt: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserOPENIDAltWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates a Pyramid access authentication token using OpenID authentication parameter map and custom data
    ApiResponse<string> response = apiInstance.AuthenticateUserOPENIDAltWithHttpInfo(userOpenIdCredentials);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserOPENIDAltWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userOpenIdCredentials** | [**UserOpenIdCredentials**](UserOpenIdCredentials.md) |  |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateusersaml"></a>
# **AuthenticateUserSAML**
> string AuthenticateUserSAML (string token)

Generates a Pyramid access authentication token using SAML authentication tokens

The security token is a string that needs to be embedded in every API call to ensure the API calls are authorized. If saved as a cookie in a web browser, it can be used (for the authenticated user) to auto-login into the application. The assumption is that the user has already authenticated via SAML before attempting to authenticate into Pyramid.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserSAMLExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var token = "token_example";  // string | The SAML assertion token

            try
            {
                // Generates a Pyramid access authentication token using SAML authentication tokens
                string result = apiInstance.AuthenticateUserSAML(token);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserSAML: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserSAMLWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates a Pyramid access authentication token using SAML authentication tokens
    ApiResponse<string> response = apiInstance.AuthenticateUserSAMLWithHttpInfo(token);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserSAMLWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **token** | **string** | The SAML assertion token |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateusersamlalt"></a>
# **AuthenticateUserSAMLAlt**
> string AuthenticateUserSAMLAlt (UserSamlCredentials userSamlCredentials)

Generates a Pyramid access authentication token using SAML authentication tokens and custom data

The security token is a string that needs to be embedded in every API call to ensure the API calls are authorized. If saved as a cookie in a web browser, it can be used (for the authenticated user) to auto-login into the application. The assumption is that the user has already authenticated via SAML before attempting to authenticate into Pyramid.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserSAMLAltExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);
            var userSamlCredentials = new UserSamlCredentials(); // UserSamlCredentials | 

            try
            {
                // Generates a Pyramid access authentication token using SAML authentication tokens and custom data
                string result = apiInstance.AuthenticateUserSAMLAlt(userSamlCredentials);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserSAMLAlt: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserSAMLAltWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates a Pyramid access authentication token using SAML authentication tokens and custom data
    ApiResponse<string> response = apiInstance.AuthenticateUserSAMLAltWithHttpInfo(userSamlCredentials);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserSAMLAltWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userSamlCredentials** | [**UserSamlCredentials**](UserSamlCredentials.md) |  |  |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="authenticateuserwindows"></a>
# **AuthenticateUserWindows**
> string AuthenticateUserWindows ()

Generates a Pyramid access authentication token using windows authentication tokens

The security token is a string that needs to be embedded in every API call to ensure the API calls are authorized. If saved as a cookie in a web browser, it can be used (for the authenticated user) to auto-login into the application.Importantly, the web browser must support Windows Authentication and the authentication METHOD must be set to 'Windows Authentication' in Pyramid.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class AuthenticateUserWindowsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            var apiInstance = new AuthenticationServiceApi(config);

            try
            {
                // Generates a Pyramid access authentication token using windows authentication tokens
                string result = apiInstance.AuthenticateUserWindows();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserWindows: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AuthenticateUserWindowsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generates a Pyramid access authentication token using windows authentication tokens
    ApiResponse<string> response = apiInstance.AuthenticateUserWindowsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthenticationServiceApi.AuthenticateUserWindowsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain;charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The response is the security token as a base64 string. It is usually stored in a cookie. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

