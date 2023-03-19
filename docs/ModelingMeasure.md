# PyramidAnalytics.Api3.Model.ModelingMeasure
Definition of a measure in the model definition, contains column unique identifies, aggregation, etc. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MeasureId** | **Guid** | The measure&#39;s System ID | [optional] 
**DisplayName** | **string** | The measure&#39;s display name | [optional] 
**UniqueName** | **string** | The measure&#39;s Unique identifier | [optional] 
**Description** | **string** | The measure&#39;s description | [optional] 
**SourceColumnUniqueName** | **string** | The Unique identifier of the column this measure is based on | [optional] 
**Expression** | **string** | The expression inside the aggregation type | [optional] 
**Format** | **string** | The measure&#39;s format string | [optional] 
**AggregationType** | **string** | The measure&#39;s aggregation type (sum,count,etc) | [optional] 
**DataType** | **string** | The measure&#39;s data type | [optional] 
**DisplayFolder** | **string** | The measure&#39;s display folder name | [optional] 
**MeasureType** | **string** | The measure&#39;s Attribute Type | [optional] 
**MeasureGroup** | **string** | This measure&#39;s measure group name | [optional] 
**Scale** | **int** | The measure&#39;s scale | [optional] 
**SuffixColumnUniqueName** | **string** | The column to take the suffix from | [optional] 
**PrefixColumnUniqueName** | **string** | The column to take the prefix from | [optional] 
**InheritanceType** | **string** | Value used to determine the type of the item receiving, use the class name | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

