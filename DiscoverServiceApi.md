# PyramidAnalytics.Api3.Api.DiscoverServiceApi

All URIs are relative to *http://Domain*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SaveDiscover**](DiscoverServiceApi.md#savediscover) | **POST** /API3/discover/saveDiscover | save a discover. |

<a name="savediscover"></a>
# **SaveDiscover**
> Guid SaveDiscover (ApiDiscover apiDiscover)

save a discover.

Use this in conjunction with other APIs

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class SaveDiscoverExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new DiscoverServiceApi(config);
            var apiDiscover = new ApiDiscover(); // ApiDiscover | 

            try
            {
                // save a discover.
                Guid result = apiInstance.SaveDiscover(apiDiscover);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscoverServiceApi.SaveDiscover: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveDiscoverWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // save a discover.
    ApiResponse<Guid> response = apiInstance.SaveDiscoverWithHttpInfo(apiDiscover);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscoverServiceApi.SaveDiscoverWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **apiDiscover** | [**ApiDiscover**](ApiDiscover.md) |  |  |

### Return type

**Guid**

### Authorization

[paToken](../README.md#paToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Returns the created discover ID |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

