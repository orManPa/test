# PyramidAnalytics.Api3.Model.ApiDiscover
Describes the metadata of the discover object

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConnectionID** | **Guid** | The ID of the connection object representing the details of the data sources. | 
**FolderId** | **Guid** | the destination folder for the item | 
**ItemName** | **string** | the name of the item | 
**Description** | **string** | The description of the item | [optional] 
**Tags** | **List&lt;string&gt;** | file tags for filtering | [optional] 
**ThemeId** | **string** | themeId from pyramid application | 
**Visual** | **string** | Defines The Visual of the current discover | 
**QueryFeatures** | [**QueryFeatures**](QueryFeatures.md) |  | [optional] 
**DropZones** | [**DropZones**](DropZones.md) |  | 
**ValueChipReflectionType** | **string** | Defines the axis position of the value selections | [optional] 
**ValueChipIndex** | **int** | the index for the generated value chip in the reflected dropzone, negative values will be indexes from the end eg. -1 is the last element, -2 is one before and so on | [optional] [default to -1]
**InheritanceType** | **string** | Value used to determine the type of the item receiving, use the class name | [optional] [default to "ApiDiscover"]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

