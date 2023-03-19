# PyramidAnalytics.Api3.Api.AccessServiceApi

All URIs are relative to *http://Domain*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAllRoles**](AccessServiceApi.md#getallroles) | **POST** /API3/access/getAllRoles | Get a list of all roles in the system |
| [**GetAllTenants**](AccessServiceApi.md#getalltenants) | **POST** /API3/access/getAllTenants | Get all tenants and their related metadata |
| [**GetMe**](AccessServiceApi.md#getme) | **POST** /API3/access/getMe | Returns the user info for the currently authenticated user |
| [**GetUsersByName**](AccessServiceApi.md#getusersbyname) | **POST** /API3/access/getUsersByName | Returns a user object which matches the user&#39;s login name. |

<a name="getallroles"></a>
# **GetAllRoles**
> List&lt;ItemId&gt; GetAllRoles ()

Get a list of all roles in the system

This method only returns role ID's. Use this method with 'getRoleById' to get the role object.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class GetAllRolesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new AccessServiceApi(config);

            try
            {
                // Get a list of all roles in the system
                List<ItemId> result = apiInstance.GetAllRoles();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccessServiceApi.GetAllRoles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllRolesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a list of all roles in the system
    ApiResponse<List<ItemId>> response = apiInstance.GetAllRolesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccessServiceApi.GetAllRolesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;ItemId&gt;**](ItemId.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Returns a generic response object with the list of all role IDs |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getalltenants"></a>
# **GetAllTenants**
> List&lt;AdminMultiTenantData&gt; GetAllTenants ()

Get all tenants and their related metadata

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class GetAllTenantsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new AccessServiceApi(config);

            try
            {
                // Get all tenants and their related metadata
                List<AdminMultiTenantData> result = apiInstance.GetAllTenants();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccessServiceApi.GetAllTenants: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllTenantsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all tenants and their related metadata
    ApiResponse<List<AdminMultiTenantData>> response = apiInstance.GetAllTenantsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccessServiceApi.GetAllTenantsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;AdminMultiTenantData&gt;**](AdminMultiTenantData.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tenant response object with details of each tenant found in the system. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getme"></a>
# **GetMe**
> PyramidViewUserObject GetMe ()

Returns the user info for the currently authenticated user

Use this method to extact details for the account running the API calls

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class GetMeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new AccessServiceApi(config);

            try
            {
                // Returns the user info for the currently authenticated user
                PyramidViewUserObject result = apiInstance.GetMe();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccessServiceApi.GetMe: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetMeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Returns the user info for the currently authenticated user
    ApiResponse<PyramidViewUserObject> response = apiInstance.GetMeWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccessServiceApi.GetMeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**PyramidViewUserObject**](PyramidViewUserObject.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getusersbyname"></a>
# **GetUsersByName**
> List&lt;PyramidViewUserObject&gt; GetUsersByName (string userName)

Returns a user object which matches the user's login name.

The user object can be used in other operations where it is required.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class GetUsersByNameExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new AccessServiceApi(config);
            var userName = "userName_example";  // string | The user's login name

            try
            {
                // Returns a user object which matches the user's login name.
                List<PyramidViewUserObject> result = apiInstance.GetUsersByName(userName);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AccessServiceApi.GetUsersByName: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetUsersByNameWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Returns a user object which matches the user's login name.
    ApiResponse<List<PyramidViewUserObject>> response = apiInstance.GetUsersByNameWithHttpInfo(userName);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AccessServiceApi.GetUsersByNameWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userName** | **string** | The user&#39;s login name |  |

### Return type

[**List&lt;PyramidViewUserObject&gt;**](PyramidViewUserObject.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User response object with details of the user found in the system. |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

