# PyramidAnalytics.Api3.Model.ModelingColumn
Definition of a table column in the model.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ColumnId** | **Guid** | The column&#39;s system ID | [optional] 
**DisplayName** | **string** | The column&#39;s display name | [optional] 
**Description** | **string** | The column&#39;s description | [optional] 
**Format** | **string** | The column&#39;s data format | [optional] 
**UniqueName** | **string** | The column&#39;s unique identifier, used in relationships, hierarchies and measures | [optional] 
**ParentUniqueName** | **string** | Unique identifier of the table that contains this column | [optional] 
**SourceColumnName** | **string** | The column&#39;s name in the database | [optional] 
**Type** | **string** | The column&#39;s data type | [optional] 
**ColumnType** | **string** | Column type | [optional] 
**DefaultSortColumnUniqueName** | **string** | Unique identifier of the default column to sort by when the user sorts by this column | [optional] 
**IsDefaultSortDescending** | **bool** | Is the default sorting descending | [optional] 
**Size** | **int** | Size of the source column type (string length or decimal precision) | [optional] 
**Scale** | **int** | Scale of the source column type (if decimal) | [optional] 
**IsVisible** | **bool** | Is the column displayed in the  | [optional] 
**IsSecurity** | **bool** | Is this a column used in the security panel | [optional] 
**IsDistribution** | **bool** | Is column for publication distribution | [optional] 
**IsUniqueIdentifier** | **bool** | Is column for experiment unique identifier | [optional] 
**DisplayFolder** | **string** | Column&#39;s display folder name | [optional] 
**IsIndexed** | **bool** | Is this column indexed in the source database | [optional] 
**ColumnIndex** | **int** | Index of this column in the table, start at 0 | [optional] 
**HasMultiMeasures** | **bool** | Boolean indicating if this column has multi-measures | [optional] 
**IsAggregatable** | **bool** | Can this column be aggregated | [optional] 
**ColumnCategory** | **string** | Predefined category of this column (time intelligence part, location part, etc) | [optional] 
**CustomColumnData** | [**ModelingCustomColumnData**](ModelingCustomColumnData.md) |  | [optional] 
**CustomCategoryId** | **string** | User defined category of this column | [optional] 
**KeyColumn** | **string** | Unique identifier of the key column for this column | [optional] 
**HasDefaultMember** | **bool** | Does this column has a default member | [optional] 
**Unicode** | **bool** |  | [optional] 
**InheritanceType** | **string** | Value used to determine the type of the item receiving, use the class name | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

