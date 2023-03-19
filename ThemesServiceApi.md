# PyramidAnalytics.Api3.Api.ThemesServiceApi

All URIs are relative to *http://Domain*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FindThemeByName**](ThemesServiceApi.md#findthemebyname) | **POST** /API3/themes/findThemeByName | Searches for a theme based on search criteria. |

<a name="findthemebyname"></a>
# **FindThemeByName**
> List&lt;ThemeListObject&gt; FindThemeByName (SearchCriteria searchCriteria)

Searches for a theme based on search criteria.

Use this in conjunction with other theme based APIs

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class FindThemeByNameExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new ThemesServiceApi(config);
            var searchCriteria = new SearchCriteria(); // SearchCriteria | 

            try
            {
                // Searches for a theme based on search criteria.
                List<ThemeListObject> result = apiInstance.FindThemeByName(searchCriteria);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ThemesServiceApi.FindThemeByName: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FindThemeByNameWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches for a theme based on search criteria.
    ApiResponse<List<ThemeListObject>> response = apiInstance.FindThemeByNameWithHttpInfo(searchCriteria);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ThemesServiceApi.FindThemeByNameWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **searchCriteria** | [**SearchCriteria**](SearchCriteria.md) |  |  |

### Return type

[**List&lt;ThemeListObject&gt;**](ThemeListObject.md)

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

