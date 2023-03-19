# PyramidAnalytics.Api3.Model.AdminMultiTenantData
The tenant object contains all relevant meta-data for the tenant.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The tenant&#39;s system ID | [optional] 
**Name** | **string** | The tenant&#39;s name | [optional] 
**ViewerSeats** | **int** | The total number of viewer licenses for the tenant | [optional] 
**UsedViewerSeats** | **int** | The total number of USED viewer licenses for the tenant | [optional] 
**ProSeats** | **int** | The total number of professional licenses for the tenant | [optional] 
**UsedProSeats** | **int** | The total number of USED professional licenses for the tenant | [optional] 
**AnalystSeats** | **int** | The total number of analyst licenses for the tenant | [optional] 
**UsedAnalystSeats** | **int** | The total number of USED analyst licenses for the tenant | [optional] 
**BasicSeats** | **int** | The total number of basic licenses for the tenant | [optional] 
**UsedBasicSeats** | **int** | The total number of USED basic licenses for the tenant | [optional] 
**TenantSettings** | [**TenantSettings**](TenantSettings.md) |  | [optional] 
**PulseKey** | **string** | The PULSE server key for the tenant | [optional] 
**SelectedUserDefaultsId** | **string** |  | [optional] 
**SelectedUserDefaultsName** | **string** |  | [optional] 
**DefaultThemeId** | **string** |  | [optional] 
**DefaultEmailTemplateId** | **string** |  | [optional] 
**HomepageTemplate** | **string** |  | [optional] 
**AdminTemplate** | **string** |  | [optional] 
**EmbedTemplate** | **string** |  | [optional] 
**DefaultAiServer** | **string** | The id of the default ai server of the tenant | [optional] 
**UserDefaultsOverridable** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

