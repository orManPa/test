# PyramidAnalytics.Api3 - the C# library for the Pyramid Analytics Web API

Pyramid Analytics Web API enables user applications to manage their pyramid
                                            data and settings

This C# SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1
- SDK version: 1.2.3
- Build package: org.openapitools.codegen.languages.CSharpNetCoreClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET Core >=1.0
- .NET Framework >=4.6
- Mono/Xamarin >=vNext

<a name="dependencies"></a>
## Dependencies

- [RestSharp](https://www.nuget.org/packages/RestSharp) - 106.13.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 13.0.1 or later
- [JsonSubTypes](https://www.nuget.org/packages/JsonSubTypes/) - 1.8.0 or later
- [System.ComponentModel.Annotations](https://www.nuget.org/packages/System.ComponentModel.Annotations) - 5.0.0 or later

The DLLs included in the package may not be the latest version. We recommend using [NuGet](https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package RestSharp
Install-Package Newtonsoft.Json
Install-Package JsonSubTypes
Install-Package System.ComponentModel.Annotations
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742).
NOTE: RestSharp for .Net Core creates a new socket for each api call, which can lead to a socket exhaustion problem. See [RestSharp#1406](https://github.com/restsharp/RestSharp/issues/1406).

<a name="installation"></a>
## Installation
Generate the DLL using your preferred tool (e.g. `dotnet build`)

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;
```
<a name="usage"></a>
## Usage

To use the API client with a HTTP proxy, setup a `System.Net.WebProxy`
```csharp
Configuration c = new Configuration();
System.Net.WebProxy webProxy = new System.Net.WebProxy("http://myProxyUrl:80/");
webProxy.Credentials = System.Net.CredentialCache.DefaultCredentials;
c.Proxy = webProxy;
```

<a name="getting-started"></a>
## Getting Started

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using PyramidAnalytics.Api3.Api;
using PyramidAnalytics.Api3.Client;
using PyramidAnalytics.Api3.Model;

namespace Example
{
    public class Example
    {
        public static void Main()
        {

            Configuration config = new Configuration();
            config.BasePath = "http://Domain";
            // Configure API key authorization: paToken
            config.ApiKey.Add("paToken", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.ApiKeyPrefix.Add("paToken", "Bearer");

            var apiInstance = new AccessServiceApi(config);

            try
            {
                // Get a list of all roles in the system
                List<ItemId> result = apiInstance.GetAllRoles();
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling AccessServiceApi.GetAllRoles: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }

        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *http://Domain*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccessServiceApi* | [**GetAllRoles**](docs\AccessServiceApi.md#getallroles) | **POST** /API3/access/getAllRoles | Get a list of all roles in the system
*AccessServiceApi* | [**GetAllTenants**](docs\AccessServiceApi.md#getalltenants) | **POST** /API3/access/getAllTenants | Get all tenants and their related metadata
*AccessServiceApi* | [**GetMe**](docs\AccessServiceApi.md#getme) | **POST** /API3/access/getMe | Returns the user info for the currently authenticated user
*AccessServiceApi* | [**GetUsersByName**](docs\AccessServiceApi.md#getusersbyname) | **POST** /API3/access/getUsersByName | Returns a user object which matches the user's login name.
*AuthenticationServiceApi* | [**AuthenticateUser**](docs\AuthenticationServiceApi.md#authenticateuser) | **POST** /API3/auth/authenticateUser | Generates an access authentication token for the given user to use the API functions or login to the application.
*AuthenticationServiceApi* | [**AuthenticateUserByToken**](docs\AuthenticationServiceApi.md#authenticateuserbytoken) | **POST** /API3/auth/authenticateUserByToken | Generates an access authentication token for a given user without their password, using an administrative token to authorize login to the application instead.
*AuthenticationServiceApi* | [**AuthenticateUserEmbed**](docs\AuthenticationServiceApi.md#authenticateuserembed) | **POST** /API3/auth/authenticateUserEmbed | Generates an access authentication token for the given user to use the embedded content functionality.
*AuthenticationServiceApi* | [**AuthenticateUserEmbedByToken**](docs\AuthenticationServiceApi.md#authenticateuserembedbytoken) | **POST** /API3/auth/authenticateUserEmbedByToken | Generates an access authentication token for embedding content, for a given user without their password, using an administrative token.
*AuthenticationServiceApi* | [**AuthenticateUserEmbedOPENID**](docs\AuthenticationServiceApi.md#authenticateuserembedopenid) | **POST** /API3/auth/authenticateUserEmbedOPENID | Generates a Pyramid access authentication token for embedding using OpenID parameter map
*AuthenticationServiceApi* | [**AuthenticateUserEmbedSAML**](docs\AuthenticationServiceApi.md#authenticateuserembedsaml) | **POST** /API3/auth/authenticateUserEmbedSAML | Generates a Pyramid access authentication token for embedding using SAML authentication tokens
*AuthenticationServiceApi* | [**AuthenticateUserEmbedWindows**](docs\AuthenticationServiceApi.md#authenticateuserembedwindows) | **POST** /API3/auth/authenticateUserEmbedWindows | Generates a Pyramid access authentication token for embedding using Windows Authentication tokens
*AuthenticationServiceApi* | [**AuthenticateUserOPENID**](docs\AuthenticationServiceApi.md#authenticateuseropenid) | **POST** /API3/auth/authenticateUserOPENID | Generates a Pyramid access authentication token using OpenID authentication parameter map
*AuthenticationServiceApi* | [**AuthenticateUserOPENIDAlt**](docs\AuthenticationServiceApi.md#authenticateuseropenidalt) | **POST** /API3/auth/authenticateUserOPENIDAlt | Generates a Pyramid access authentication token using OpenID authentication parameter map and custom data
*AuthenticationServiceApi* | [**AuthenticateUserSAML**](docs\AuthenticationServiceApi.md#authenticateusersaml) | **POST** /API3/auth/authenticateUserSAML | Generates a Pyramid access authentication token using SAML authentication tokens
*AuthenticationServiceApi* | [**AuthenticateUserSAMLAlt**](docs\AuthenticationServiceApi.md#authenticateusersamlalt) | **POST** /API3/auth/authenticateUserSAMLAlt | Generates a Pyramid access authentication token using SAML authentication tokens and custom data
*AuthenticationServiceApi* | [**AuthenticateUserWindows**](docs\AuthenticationServiceApi.md#authenticateuserwindows) | **POST** /API3/auth/authenticateUserWindows | Generates a Pyramid access authentication token using windows authentication tokens
*ContentServiceApi* | [**CreateNewFolder**](docs\ContentServiceApi.md#createnewfolder) | **POST** /API3/content/createNewFolder | Adds a new folder to the application
*ContentServiceApi* | [**FindContentItem**](docs\ContentServiceApi.md#findcontentitem) | **POST** /API3/content/findContentItem | Returns a list of content items based on search criteria
*ContentServiceApi* | [**GetFolderItems**](docs\ContentServiceApi.md#getfolderitems) | **POST** /API3/content/getFolderItems | Gets a list of content items in a given folder.
*DataSourcesServiceApi* | [**FindDatabaseByName**](docs\DataSourcesServiceApi.md#finddatabasebyname) | **POST** /API3/dataSources/findDatabaseByName | Return a list of databases based on search string and parent server ID
*DataSourcesServiceApi* | [**FindModelConnectionByName**](docs\DataSourcesServiceApi.md#findmodelconnectionbyname) | **POST** /API3/dataSources/findModelConnectionByName | Return a list of models based on search string and its parent database ID
*DataSourcesServiceApi* | [**FindServerByName**](docs\DataSourcesServiceApi.md#findserverbyname) | **POST** /API3/dataSources/findServerByName | Return a list of servers based on search string
*DataSourcesServiceApi* | [**GetDataModelStructureByConnection**](docs\DataSourcesServiceApi.md#getdatamodelstructurebyconnection) | **POST** /API3/dataSources/getDataModelStructureByConnection | Returns the structural definition of a materialized data model in JSON format by the model connectionId.
*DataSourcesServiceApi* | [**SearchModelConnection**](docs\DataSourcesServiceApi.md#searchmodelconnection) | **POST** /API3/dataSources/searchModelConnection | Return a list of data sources connections and their properties based on search parameters
*DiscoverServiceApi* | [**SaveDiscover**](docs\DiscoverServiceApi.md#savediscover) | **POST** /API3/discover/saveDiscover | save a discover.
*FormulateServiceApi* | [**SaveCustomFormula**](docs\FormulateServiceApi.md#savecustomformula) | **POST** /API3/formulate/saveCustomFormula | Save Custom Formula.
*FormulateServiceApi* | [**SaveCustomList**](docs\FormulateServiceApi.md#savecustomlist) | **POST** /API3/formulate/saveCustomList | Save Custom List.
*ThemesServiceApi* | [**FindThemeByName**](docs\ThemesServiceApi.md#findthemebyname) | **POST** /API3/themes/findThemeByName | Searches for a theme based on search criteria.


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.AdditionalValuesDropZone](docs\AdditionalValuesDropZone.md)
 - [Model.AdminMultiTenantData](docs\AdminMultiTenantData.md)
 - [Model.ApiCustomFormula](docs\ApiCustomFormula.md)
 - [Model.ApiCustomFormulaOlapProperties](docs\ApiCustomFormulaOlapProperties.md)
 - [Model.ApiCustomList](docs\ApiCustomList.md)
 - [Model.ApiDiscover](docs\ApiDiscover.md)
 - [Model.ApiDropZoneChip](docs\ApiDropZoneChip.md)
 - [Model.ApiHierarchy](docs\ApiHierarchy.md)
 - [Model.ApiHierarchyElements](docs\ApiHierarchyElements.md)
 - [Model.ApiMeasure](docs\ApiMeasure.md)
 - [Model.ArgumentValue](docs\ArgumentValue.md)
 - [Model.BaseScriptData](docs\BaseScriptData.md)
 - [Model.CalendarTimeSettings](docs\CalendarTimeSettings.md)
 - [Model.CategoriesDropZone](docs\CategoriesDropZone.md)
 - [Model.ColorDropZone](docs\ColorDropZone.md)
 - [Model.ColumnFunction](docs\ColumnFunction.md)
 - [Model.ColumnsDropZone](docs\ColumnsDropZone.md)
 - [Model.ConnectedItemsSearchCriteria](docs\ConnectedItemsSearchCriteria.md)
 - [Model.ConnectionSearchCriteria](docs\ConnectionSearchCriteria.md)
 - [Model.ConnectionStringProperties](docs\ConnectionStringProperties.md)
 - [Model.ContentSearchParamsObject](docs\ContentSearchParamsObject.md)
 - [Model.CrossSet](docs\CrossSet.md)
 - [Model.CustomColor](docs\CustomColor.md)
 - [Model.CustomMemberData](docs\CustomMemberData.md)
 - [Model.Datapoint](docs\Datapoint.md)
 - [Model.DateSelection](docs\DateSelection.md)
 - [Model.DetailsDropZone](docs\DetailsDropZone.md)
 - [Model.DropZones](docs\DropZones.md)
 - [Model.ElementFunction](docs\ElementFunction.md)
 - [Model.ElementFunctionArgument](docs\ElementFunctionArgument.md)
 - [Model.ElementSelection](docs\ElementSelection.md)
 - [Model.ElementsGrouping](docs\ElementsGrouping.md)
 - [Model.FilterDropZone](docs\FilterDropZone.md)
 - [Model.FormulaElement](docs\FormulaElement.md)
 - [Model.FunctionData](docs\FunctionData.md)
 - [Model.FunctionDependency](docs\FunctionDependency.md)
 - [Model.GeoDropZone](docs\GeoDropZone.md)
 - [Model.IndicatorDropZone](docs\IndicatorDropZone.md)
 - [Model.ItemId](docs\ItemId.md)
 - [Model.LabelsDropZone](docs\LabelsDropZone.md)
 - [Model.MaterializedItemObject](docs\MaterializedItemObject.md)
 - [Model.MeasureGroup](docs\MeasureGroup.md)
 - [Model.MemberSelection](docs\MemberSelection.md)
 - [Model.ModelAttribute](docs\ModelAttribute.md)
 - [Model.ModelDataFlowSourceInfo](docs\ModelDataFlowSourceInfo.md)
 - [Model.ModelSyncColumnsSettings](docs\ModelSyncColumnsSettings.md)
 - [Model.ModelingAggregationMapping](docs\ModelingAggregationMapping.md)
 - [Model.ModelingColumn](docs\ModelingColumn.md)
 - [Model.ModelingCustomColumnData](docs\ModelingCustomColumnData.md)
 - [Model.ModelingHierarchy](docs\ModelingHierarchy.md)
 - [Model.ModelingHierarchyLevel](docs\ModelingHierarchyLevel.md)
 - [Model.ModelingMeasure](docs\ModelingMeasure.md)
 - [Model.ModelingModel](docs\ModelingModel.md)
 - [Model.ModelingProperty](docs\ModelingProperty.md)
 - [Model.ModelingRelationship](docs\ModelingRelationship.md)
 - [Model.ModelingRelationshipColumnPair](docs\ModelingRelationshipColumnPair.md)
 - [Model.ModelingServerInfo](docs\ModelingServerInfo.md)
 - [Model.ModelingTable](docs\ModelingTable.md)
 - [Model.ModifiedItemsResult](docs\ModifiedItemsResult.md)
 - [Model.MotionDropZone](docs\MotionDropZone.md)
 - [Model.NewFolderApiData](docs\NewFolderApiData.md)
 - [Model.ParameterSelection](docs\ParameterSelection.md)
 - [Model.PatternMatchDefinition](docs\PatternMatchDefinition.md)
 - [Model.PromSelection](docs\PromSelection.md)
 - [Model.PromSelectionWrapper](docs\PromSelectionWrapper.md)
 - [Model.PropertyOverrideSelection](docs\PropertyOverrideSelection.md)
 - [Model.PropertySelection](docs\PropertySelection.md)
 - [Model.PyramidContentItem](docs\PyramidContentItem.md)
 - [Model.PyramidViewUserObject](docs\PyramidViewUserObject.md)
 - [Model.QomCustomSet](docs\QomCustomSet.md)
 - [Model.QomSelection](docs\QomSelection.md)
 - [Model.QomSelectionProperties](docs\QomSelectionProperties.md)
 - [Model.QueryFeatures](docs\QueryFeatures.md)
 - [Model.QueryInputSelection](docs\QueryInputSelection.md)
 - [Model.RowsDropZone](docs\RowsDropZone.md)
 - [Model.SearchCriteria](docs\SearchCriteria.md)
 - [Model.SetData](docs\SetData.md)
 - [Model.ShapeDropZone](docs\ShapeDropZone.md)
 - [Model.SizeDropZone](docs\SizeDropZone.md)
 - [Model.SourceDropZone](docs\SourceDropZone.md)
 - [Model.StatusDropZone](docs\StatusDropZone.md)
 - [Model.Stream](docs\Stream.md)
 - [Model.StreamPairApiDropZoneTypeDropZoneBase](docs\StreamPairApiDropZoneTypeDropZoneBase.md)
 - [Model.TargetDropZone](docs\TargetDropZone.md)
 - [Model.TenantSettings](docs\TenantSettings.md)
 - [Model.ThemeListObject](docs\ThemeListObject.md)
 - [Model.TooltipDropZone](docs\TooltipDropZone.md)
 - [Model.TrellisHorizontalDropZone](docs\TrellisHorizontalDropZone.md)
 - [Model.TrellisVerticalDropZone](docs\TrellisVerticalDropZone.md)
 - [Model.UserCredentials](docs\UserCredentials.md)
 - [Model.UserOpenIdCredentials](docs\UserOpenIdCredentials.md)
 - [Model.UserSamlCredentials](docs\UserSamlCredentials.md)
 - [Model.UserTokenCredentials](docs\UserTokenCredentials.md)
 - [Model.ValueSelection](docs\ValueSelection.md)
 - [Model.ValueSelectionProperties](docs\ValueSelectionProperties.md)
 - [Model.ValuesDropZone](docs\ValuesDropZone.md)
 - [Model.XAxisDropZone](docs\XAxisDropZone.md)
 - [Model.YAxisDropZone](docs\YAxisDropZone.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="paToken"></a>
### paToken

- **Type**: API key
- **API key parameter name**: paToken
- **Location**: HTTP header
