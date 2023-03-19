# PyramidAnalytics.Api3.Model.ModelingModel
The model definition that contains details of tables, their relationships and joins, and measures.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ModelId** | **Guid** | The model&#39;s system ID | [optional] 
**DisplayName** | **string** | The model&#39;s display name | [optional] 
**Description** | **string** | A description of the model | [optional] 
**Tables** | [**List&lt;ModelingTable&gt;**](ModelingTable.md) | A list of tables/dimensions in the model | [optional] 
**Relationships** | [**List&lt;ModelingRelationship&gt;**](ModelingRelationship.md) | A list of the relationships between tables in the model | [optional] 
**ServerId** | **string** | The host server&#39;s name | [optional] 
**DatabaseName** | **string** | The model&#39;s database name | [optional] 
**ModelType** | **string** | The type of model. | [optional] 
**ModelDataFlowSourceInfo** | [**ModelDataFlowSourceInfo**](ModelDataFlowSourceInfo.md) |  | [optional] 
**IsAutoIndexing** | **bool** | Set to true for heuristic index creation | [optional] 
**DefaultMeasureUniqueName** | **string** | Unique identifier of the default measure | [optional] 
**MeasureGroups** | [**List&lt;MeasureGroup&gt;**](MeasureGroup.md) | The model&#39;s measure groups.  | [optional] 
**Culture** | **string** | The model&#39;s culture name | [optional] 
**DisableCacheMode** | **bool** | Should disable cache | [optional] 
**AdditionalLanguages** | **Dictionary&lt;string, string&gt;** | Additional languages in the model | [optional] 
**Arrange** | **bool** | Should auto-arrange | [optional] 
**ServerInfo** | [**ModelingServerInfo**](ModelingServerInfo.md) |  | [optional] 
**NullMemberCaption** | **string** |  | [optional] 
**CalculatedMembersByAttribute** | **Dictionary&lt;string, List&lt;string&gt;&gt;** |  | [optional] 
**SyncColumnsSettings** | [**List&lt;ModelSyncColumnsSettings&gt;**](ModelSyncColumnsSettings.md) | settings for sync columns by schedule. defines an aggregation and visibility for each new column data type. | [optional] 
**LinkRouterType** | **string** |  | [optional] 
**ProcessDate** | **DateTime** |  | [optional] 
**MaterializedItemType** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

