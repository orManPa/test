# PyramidAnalytics.Api3.Model.ModelingHierarchy
Hierarchy definition in the model. A hierarchy is defined by a list of levels, each defined by a column

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**HierarchyId** | **Guid** | The hierarchy&#39;s System ID | [optional] 
**Levels** | [**List&lt;ModelingHierarchyLevel&gt;**](ModelingHierarchyLevel.md) | The hierarchy levels | [optional] 
**DisplayName** | **string** | The hierarchy&#39;s Display Name | [optional] 
**UniqueName** | **string** | The hierarchy&#39;s Unique identifier | [optional] 
**DisplayFolder** | **string** | The hierarchy&#39;s display folder name | [optional] 
**Description** | **string** | The hierarchy&#39;s description | [optional] 
**IsAggregatable** | **bool** | Is it possible to aggregate by this hierarchy | [optional] 
**HasDefaultMember** | **bool** | Does this hierarchy have a default member | [optional] 
**HierarchyType** | **string** | The hierarchy&#39;s type | [optional] 
**HierarchyCategory** | **string** | Predefined hierarchy category | [optional] 
**ParentKeySourceColumnUniqueName** | **string** | Parent-Child hierarchy&#39;s parent column | [optional] 
**KeySourceColumnUniqueName** | **string** | Parent-Child hierarchy&#39;s key column | [optional] 
**OrderSourceColumnUniqueName** | **string** | Parent-Child hierarchy&#39;s order column | [optional] 
**CaptionSourceColumnUniqueName** | **string** | Parent-Child hierarchy&#39;s caption column | [optional] 
**UnaryOperatorSourceColumnUniqueName** | **string** | Parent-Child hierarchy&#39;s unary-operator column | [optional] 
**ParentChildRollupType** | **string** | Parent-Child hierarchy&#39;s rollup type | [optional] 
**ParentChildOrphanHandlingType** | **string** | Parent-Child hierarchy&#39;s handling for orphan nodes | [optional] 
**CaptionColumnUniqueNameOrNullIfSelf** | **string** |  | [optional] 
**OrderColumnUniqueNameOrNullIfSelf** | **string** |  | [optional] 
**StartingLevel** | **int** |  | [optional] 
**InheritanceType** | **string** | Value used to determine the type of the item receiving, use the class name | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

