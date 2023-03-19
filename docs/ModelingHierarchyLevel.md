# PyramidAnalytics.Api3.Model.ModelingHierarchyLevel
Definition of a hierarchy level in the model definition, contains source column identifier.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LevelId** | **Guid** | System ID of this hierarchy level | [optional] 
**LevelNumber** | **int** | Level number | [optional] 
**UniqueName** | **string** | Unique identifier of this hierarchy level | [optional] 
**DisplayName** | **string** | Display name of this hierarchy level | [optional] 
**SourceColumnUniqueName** | **string** | Unique identifier of this level&#39;s source column | [optional] 
**CustomCategoryId** | **string** | User-defined category of this hierarchy level | [optional] 
**Description** | **string** | Description of this hierarchy level | [optional] 
**SortByColumn** | **string** | column unique name to sort by | [optional] 
**IsDefaultSortDescending** | **bool** | Is the default sorting descending | [optional] 
**Properties** | [**List&lt;ModelingProperty&gt;**](ModelingProperty.md) | Modeling properties of this hierarchy level | [optional] 
**HideMemberType** | **string** | When to hide a member on this level | [optional] 
**InheritanceType** | **string** | Value used to determine the type of the item receiving, use the class name | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

