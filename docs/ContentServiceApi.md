# PyramidAnalytics.Api3.Api.ContentServiceApi

All URIs are relative to *http://Domain*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateNewFolder**](ContentServiceApi.md#createnewfolder) | **POST** /API3/content/createNewFolder | Adds a new folder to the application |
| [**FindContentItem**](ContentServiceApi.md#findcontentitem) | **POST** /API3/content/findContentItem | Returns a list of content items based on search criteria |
| [**GetFolderItems**](ContentServiceApi.md#getfolderitems) | **POST** /API3/content/getFolderItems | Gets a list of content items in a given folder. |

<a name="createnewfolder"></a>
# **CreateNewFolder**
> ModifiedItemsResult CreateNewFolder (NewFolderApiData folderApiData)

Adds a new folder to the application

Use other methods to retrieve parent ID's and root folder ID's

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class CreateNewFolderExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new ContentServiceApi(config);
            var folderApiData = new NewFolderApiData(); // NewFolderApiData | 

            try
            {
                // Adds a new folder to the application
                ModifiedItemsResult result = apiInstance.CreateNewFolder(folderApiData);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContentServiceApi.CreateNewFolder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateNewFolderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds a new folder to the application
    ApiResponse<ModifiedItemsResult> response = apiInstance.CreateNewFolderWithHttpInfo(folderApiData);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContentServiceApi.CreateNewFolderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **folderApiData** | [**NewFolderApiData**](NewFolderApiData.md) |  |  |

### Return type

[**ModifiedItemsResult**](ModifiedItemsResult.md)

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Result object with success or failure flag and related messages. Returns the folder&#39;s ID |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="findcontentitem"></a>
# **FindContentItem**
> List&lt;PyramidContentItem&gt; FindContentItem (ContentSearchParamsObject searchParams)

Returns a list of content items based on search criteria

When setting criteria, mark the search as 'advanced' to use the extra criteria conditions

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class FindContentItemExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new ContentServiceApi(config);
            var searchParams = new ContentSearchParamsObject(); // ContentSearchParamsObject | 

            try
            {
                // Returns a list of content items based on search criteria
                List<PyramidContentItem> result = apiInstance.FindContentItem(searchParams);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContentServiceApi.FindContentItem: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FindContentItemWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Returns a list of content items based on search criteria
    ApiResponse<List<PyramidContentItem>> response = apiInstance.FindContentItemWithHttpInfo(searchParams);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContentServiceApi.FindContentItemWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **searchParams** | [**ContentSearchParamsObject**](ContentSearchParamsObject.md) |  |  |

### Return type

[**List&lt;PyramidContentItem&gt;**](PyramidContentItem.md)

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

<a name="getfolderitems"></a>
# **GetFolderItems**
> List&lt;PyramidContentItem&gt; GetFolderItems (string folderId)

Gets a list of content items in a given folder.

Use the function recursively to extract the full content tree

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class GetFolderItemsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new ContentServiceApi(config);
            var folderId = "folderId_example";  // string | The system folder ID

            try
            {
                // Gets a list of content items in a given folder.
                List<PyramidContentItem> result = apiInstance.GetFolderItems(folderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContentServiceApi.GetFolderItems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFolderItemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets a list of content items in a given folder.
    ApiResponse<List<PyramidContentItem>> response = apiInstance.GetFolderItemsWithHttpInfo(folderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContentServiceApi.GetFolderItemsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **folderId** | **string** | The system folder ID |  |

### Return type

[**List&lt;PyramidContentItem&gt;**](PyramidContentItem.md)

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

