# PyramidAnalytics.Api3.Api.DataSourcesServiceApi

All URIs are relative to *http://Domain*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FindDatabaseByName**](DataSourcesServiceApi.md#finddatabasebyname) | **POST** /API3/dataSources/findDatabaseByName | Return a list of databases based on search string and parent server ID |
| [**FindModelConnectionByName**](DataSourcesServiceApi.md#findmodelconnectionbyname) | **POST** /API3/dataSources/findModelConnectionByName | Return a list of models based on search string and its parent database ID |
| [**FindServerByName**](DataSourcesServiceApi.md#findserverbyname) | **POST** /API3/dataSources/findServerByName | Return a list of servers based on search string |
| [**GetDataModelStructureByConnection**](DataSourcesServiceApi.md#getdatamodelstructurebyconnection) | **POST** /API3/dataSources/getDataModelStructureByConnection | Returns the structural definition of a materialized data model in JSON format by the model connectionId. |
| [**SearchModelConnection**](DataSourcesServiceApi.md#searchmodelconnection) | **POST** /API3/dataSources/searchModelConnection | Return a list of data sources connections and their properties based on search parameters |

<a name="finddatabasebyname"></a>
# **FindDatabaseByName**
> List&lt;MaterializedItemObject&gt; FindDatabaseByName (ConnectedItemsSearchCriteria searchCriteria)

Return a list of databases based on search string and parent server ID

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class FindDatabaseByNameExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new DataSourcesServiceApi(config);
            var searchCriteria = new ConnectedItemsSearchCriteria(); // ConnectedItemsSearchCriteria | 

            try
            {
                // Return a list of databases based on search string and parent server ID
                List<MaterializedItemObject> result = apiInstance.FindDatabaseByName(searchCriteria);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DataSourcesServiceApi.FindDatabaseByName: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FindDatabaseByNameWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Return a list of databases based on search string and parent server ID
    ApiResponse<List<MaterializedItemObject>> response = apiInstance.FindDatabaseByNameWithHttpInfo(searchCriteria);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DataSourcesServiceApi.FindDatabaseByNameWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **searchCriteria** | [**ConnectedItemsSearchCriteria**](ConnectedItemsSearchCriteria.md) |  |  |

### Return type

[**List&lt;MaterializedItemObject&gt;**](MaterializedItemObject.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="findmodelconnectionbyname"></a>
# **FindModelConnectionByName**
> List&lt;MaterializedItemObject&gt; FindModelConnectionByName (ConnectedItemsSearchCriteria searchCriteria)

Return a list of models based on search string and its parent database ID

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class FindModelConnectionByNameExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new DataSourcesServiceApi(config);
            var searchCriteria = new ConnectedItemsSearchCriteria(); // ConnectedItemsSearchCriteria | 

            try
            {
                // Return a list of models based on search string and its parent database ID
                List<MaterializedItemObject> result = apiInstance.FindModelConnectionByName(searchCriteria);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DataSourcesServiceApi.FindModelConnectionByName: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FindModelConnectionByNameWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Return a list of models based on search string and its parent database ID
    ApiResponse<List<MaterializedItemObject>> response = apiInstance.FindModelConnectionByNameWithHttpInfo(searchCriteria);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DataSourcesServiceApi.FindModelConnectionByNameWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **searchCriteria** | [**ConnectedItemsSearchCriteria**](ConnectedItemsSearchCriteria.md) |  |  |

### Return type

[**List&lt;MaterializedItemObject&gt;**](MaterializedItemObject.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="findserverbyname"></a>
# **FindServerByName**
> List&lt;MaterializedItemObject&gt; FindServerByName (SearchCriteria searchCriteria)

Return a list of servers based on search string

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class FindServerByNameExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new DataSourcesServiceApi(config);
            var searchCriteria = new SearchCriteria(); // SearchCriteria | 

            try
            {
                // Return a list of servers based on search string
                List<MaterializedItemObject> result = apiInstance.FindServerByName(searchCriteria);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DataSourcesServiceApi.FindServerByName: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FindServerByNameWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Return a list of servers based on search string
    ApiResponse<List<MaterializedItemObject>> response = apiInstance.FindServerByNameWithHttpInfo(searchCriteria);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DataSourcesServiceApi.FindServerByNameWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **searchCriteria** | [**SearchCriteria**](SearchCriteria.md) |  |  |

### Return type

[**List&lt;MaterializedItemObject&gt;**](MaterializedItemObject.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getdatamodelstructurebyconnection"></a>
# **GetDataModelStructureByConnection**
> ModelingModel GetDataModelStructureByConnection (string connectionId)

Returns the structural definition of a materialized data model in JSON format by the model connectionId.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class GetDataModelStructureByConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new DataSourcesServiceApi(config);
            var connectionId = "connectionId_example";  // string | The model's connection system ID

            try
            {
                // Returns the structural definition of a materialized data model in JSON format by the model connectionId.
                ModelingModel result = apiInstance.GetDataModelStructureByConnection(connectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DataSourcesServiceApi.GetDataModelStructureByConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDataModelStructureByConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Returns the structural definition of a materialized data model in JSON format by the model connectionId.
    ApiResponse<ModelingModel> response = apiInstance.GetDataModelStructureByConnectionWithHttpInfo(connectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DataSourcesServiceApi.GetDataModelStructureByConnectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **connectionId** | **string** | The model&#39;s connection system ID |  |

### Return type

[**ModelingModel**](ModelingModel.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="searchmodelconnection"></a>
# **SearchModelConnection**
> List&lt;ConnectionStringProperties&gt; SearchModelConnection (ConnectionSearchCriteria searchCriteria)

Return a list of data sources connections and their properties based on search parameters

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class SearchModelConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new DataSourcesServiceApi(config);
            var searchCriteria = new ConnectionSearchCriteria(); // ConnectionSearchCriteria | 

            try
            {
                // Return a list of data sources connections and their properties based on search parameters
                List<ConnectionStringProperties> result = apiInstance.SearchModelConnection(searchCriteria);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DataSourcesServiceApi.SearchModelConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchModelConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Return a list of data sources connections and their properties based on search parameters
    ApiResponse<List<ConnectionStringProperties>> response = apiInstance.SearchModelConnectionWithHttpInfo(searchCriteria);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DataSourcesServiceApi.SearchModelConnectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **searchCriteria** | [**ConnectionSearchCriteria**](ConnectionSearchCriteria.md) |  |  |

### Return type

[**List&lt;ConnectionStringProperties&gt;**](ConnectionStringProperties.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

