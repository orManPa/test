# PyramidAnalytics.Api3.Api.FormulateServiceApi

All URIs are relative to *http://Domain*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SaveCustomFormula**](FormulateServiceApi.md#savecustomformula) | **POST** /API3/formulate/saveCustomFormula | Save Custom Formula. |
| [**SaveCustomList**](FormulateServiceApi.md#savecustomlist) | **POST** /API3/formulate/saveCustomList | Save Custom List. |

<a name="savecustomformula"></a>
# **SaveCustomFormula**
> Guid SaveCustomFormula (ApiCustomFormula customFormula)

Save Custom Formula.

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
    public class SaveCustomFormulaExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new FormulateServiceApi(config);
            var customFormula = new ApiCustomFormula(); // ApiCustomFormula | 

            try
            {
                // Save Custom Formula.
                Guid result = apiInstance.SaveCustomFormula(customFormula);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FormulateServiceApi.SaveCustomFormula: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveCustomFormulaWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Save Custom Formula.
    ApiResponse<Guid> response = apiInstance.SaveCustomFormulaWithHttpInfo(customFormula);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FormulateServiceApi.SaveCustomFormulaWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customFormula** | [**ApiCustomFormula**](ApiCustomFormula.md) |  |  |

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
| **200** | Returns the created Custom Formula ID |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="savecustomlist"></a>
# **SaveCustomList**
> Guid SaveCustomList (ApiCustomList customList)

Save Custom List.

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
    public class SaveCustomListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.AddApiKey("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("paToken", "Bearer");

            var apiInstance = new FormulateServiceApi(config);
            var customList = new ApiCustomList(); // ApiCustomList | 

            try
            {
                // Save Custom List.
                Guid result = apiInstance.SaveCustomList(customList);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FormulateServiceApi.SaveCustomList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SaveCustomListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Save Custom List.
    ApiResponse<Guid> response = apiInstance.SaveCustomListWithHttpInfo(customList);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FormulateServiceApi.SaveCustomListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customList** | [**ApiCustomList**](ApiCustomList.md) |  |  |

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
| **200** | Returns the created Custom List ID |  -  |
| **400** | Api Failed - the response from the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

