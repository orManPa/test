# PyramidAnalytics.Api3.Model.ContentSearchParamsObject
The content search object for specifying search criteria to be used in content searches.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SearchString** | **string** | The terms to be used in the search | 
**IsAdvancedSearch** | **bool** | Boolean to indicate if this is an advanced search. Advanced searches will use other provided criteria. Otherwise, the simple search will just use the search string only | [optional] 
**FilterTypes** | **List&lt;ContentSearchParamsObject.FilterTypesEnum&gt;** | A listing of different content types to narrow the search | 
**SearchMatchType** | **string** | Enumeration of the type osf search term matching | 
**StartCreatedDate** | **DateTime** | Starting date for range searching on create dates | [optional] 
**EndCreatedDate** | **DateTime** | Ending date for range searching on create dates | [optional] 
**StartModifiedDate** | **DateTime** | Starting date for range searching on modified dates | [optional] 
**EndModifiedDate** | **DateTime** | Ending date for range searching on modified dates | [optional] 
**Server** | **string** | Server name when searching by data source | [optional] 
**Model** | **string** | Model name when searching by data source | [optional] 
**DataBase** | **string** | Database name when searching by data source | [optional] 
**SearchRootFolderType** | **string** | Enumeration of which content domain to search in (private, public etc) | 
**FolderPathToSearch** | **string** | This is a folder path to use in searching. Use in the format folderA\\folderB\\..... using the folder captions, not their IDs | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

