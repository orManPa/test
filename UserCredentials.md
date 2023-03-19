# PyramidAnalytics.Api3.Model.UserCredentials
The user credential object used to set a user's login settings.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Username** | **string** | The user&#39;s login identity The format depends on the authentication provider: Its &#39;username&#39; for internal database authentication. For AD, its either UPN or &#39;domain\\username&#39;. | 
**Password** | **string** | The user&#39;s password. | 
**Domain** | **string** | The URL web domain - needed only for embedded authentication. | [optional] 
**CustomData** | **string** | Custom data input for usage within the product. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

