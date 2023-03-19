# PyramidAnalytics.Api3.Model.ModelingTable
Table definition in a model, contains table schema, name, columns, etc.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TableId** | **Guid** | The table&#39;s system ID | [optional] 
**DisplayName** | **string** | The table&#39;s display name | [optional] 
**Description** | **string** | The tables&#39;s description | [optional] 
**ModelingColumns** | [**List&lt;ModelingColumn&gt;**](ModelingColumn.md) | List of columns in this table | [optional] 
**ModelingMeasures** | [**List&lt;ModelingMeasure&gt;**](ModelingMeasure.md) | List of measures in this table | [optional] 
**ModelingHierarchies** | [**List&lt;ModelingHierarchy&gt;**](ModelingHierarchy.md) | List of hierarchies in this table | [optional] 
**UniqueName** | **string** | Unique identifier of this table | [optional] 
**SchemaName** | **string** | Schema name in the source database | [optional] 
**SourceTableName** | **string** | Tables name in the source database | [optional] 
**IsVisible** | **bool** | Visible in the relationship diagram | [optional] 
**PrimaryKeyColumnUniqueName** | **string** | Unique identifier of the primary key column of this table | [optional] 
**MeasureGroups** | **List&lt;string&gt;** | List of measure group ids | [optional] 
**CustomQuery** | **string** | If this tables is based on a query, instead of schema and table name | [optional] 
**ModelingTableType** | **string** | Table type | [optional] 
**IsML** | **bool** | Is this table a telemetry ml table | [optional] 
**SyncColumnsWithDb** | **bool** | Defines whether to synchronize columns with DB columns. | [optional] 
**IsAggregatedTable** | **bool** | Is this table is an Aggregated table | [optional] 
**TableSize** | **int** | The number of rows in the table | [optional] 
**ModelAttributeType** | **string** |  | [optional] 
**ModelingAggregations** | [**List&lt;ModelingAggregationMapping&gt;**](ModelingAggregationMapping.md) |  | [optional] 
**DisplayFolder** | **string** |  | [optional] 
**InheritanceType** | **string** | Value used to determine the type of the item receiving, use the class name | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

