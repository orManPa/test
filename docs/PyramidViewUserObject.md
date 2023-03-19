# PyramidAnalytics.Api3.Model.PyramidViewUserObject
The user object contains all relevant meta-data for the user.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The user&#39;s system ID. | 
**UserName** | **string** | The login username for the user | [optional] 
**FirstName** | **string** | The user&#39;s first name | [optional] 
**LastName** | **string** | The user&#39;s last name | [optional] 
**Email** | **string** | The user&#39;s email | [optional] 
**Phone** | **string** | The user&#39;s phone | [optional] 
**ProxyAccount** | **string** | The user&#39;s proxy account needed for connecting to different data sources | [optional] 
**Proxy2** | **string** | The user&#39;s second proxy account needed for connecting to different data sources | [optional] 
**AdminType** | **string** | The user&#39;s administration level using the admin type enumeration | [optional] 
**RoleIds** | **List&lt;string&gt;** | The user&#39;s list of roles | [optional] 
**ClientLicenseType** | **string** | The user&#39;s license type using the type enumeration | [optional] 
**StatusID** | **string** | The user&#39;s status using the status type enumeration | [optional] 
**TenantId** | **string** | The user&#39;s tenant ID | [optional] 
**CreatedDate** | **long** |  | [optional] 
**LastLoginDate** | **long** |  | [optional] 
**AdDomainName** | **string** | The AD/LDAP domain name (relevant in case the user is authenticated using AD) | [optional] 
**PrincipalName** | **string** | The user&#39;s SAML identifier (relevant in case the user is authenticated using SAML) | [optional] 
**SecondaryMobilePhone** | **string** | The user&#39;s secondary mobile phone. | [optional] 
**InheritanceType** | **string** | Value used to determine the type of the item receiving, use the class name | [optional] [default to "PyramidViewUserObject"]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

