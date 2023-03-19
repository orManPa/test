# PyramidAnalytics.Api3.Model.ApiCustomList
The Custom List To add.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConnectionID** | **Guid** | The ID of the connection object representing the details of the data sources. | 
**FolderId** | **Guid** | the destination folder for the item | 
**ItemName** | **string** | the name of the item | 
**Description** | **string** | The description of the item | [optional] 
**Tags** | **List&lt;string&gt;** | file tags for filtering | [optional] 
**FormulaSyntax** | **string** | The script representation of the calculation. | 
**ParentDimension** | **string** | Each custom formula/list must have a designated parent dimension and hierarchy; Pyramid uses heuristics to automatically assign a custom calculation to a dimension and hierarchy. | 
**ParentHierarchy** | **string** | the parent hierarchy paired with the dimension, see parentDimension - if parentDimension is \&quot;[measures]\&quot; than this is not needed | [optional] 
**InheritanceType** | **string** | Value used to determine the type of the item receiving, use the class name | [optional] [default to "ApiCustomList"]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

