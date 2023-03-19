# PyramidAnalytics.Api3.Model.ModelingRelationship
Relationship definition used in the models when joining across tables columns.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RelationshipId** | **Guid** | The relationship&#39;s system ID | [optional] 
**Columns** | [**List&lt;ModelingRelationshipColumnPair&gt;**](ModelingRelationshipColumnPair.md) | The model&#39;s system ID | [optional] 
**PrimaryTableUniqueName** | **string** | The primary table&#39;s unique name | [optional] 
**ForeignTableUniqueName** | **string** | The foreign table&#39;s unique name | [optional] 
**Type** | **string** | The join type (inner, right, left, full outer, or cross join) | [optional] 
**IsBiDirectional** | **bool** | Boolean indicating if the join is bi-directional | [optional] 
**CreationType** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

