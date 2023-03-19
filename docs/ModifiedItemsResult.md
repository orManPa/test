# PyramidAnalytics.Api3.Model.ModifiedItemsResult
Generic API response object with success or failure flag and related messages.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Success** | **bool** | Boolean showing success or failure result. | [optional] 
**ErrorMessage** | **string** | Error message in case of failure | [optional] 
**ModifiedList** | [**List&lt;ItemId&gt;**](ItemId.md) | List of item ID&#39;s that have been affected by the function call. The type of ID depends on the function. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

