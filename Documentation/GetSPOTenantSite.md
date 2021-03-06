#Get-SPOTenantSite
Office365 only: Uses the tenant API to retrieve site information.
##Syntax
```powershell
Get-SPOTenantSite [-Detailed [<SwitchParameter>]]
                  [-IncludeOneDriveSites [<SwitchParameter>]]
                  [-Force [<SwitchParameter>]]
                  [-Url <String>]
```


##Returns
>[Microsoft.Online.SharePoint.TenantAdministration.SiteProperties](https://msdn.microsoft.com/en-us/library/microsoft.online.sharepoint.tenantadministration.siteproperties.aspx)

##Parameters
Parameter|Type|Required|Description
---------|----|--------|-----------
|Detailed|SwitchParameter|False|By default, not all returned attributes are populated. This switch populates all attributes. It can take several seconds to run. Without this, some attributes will show default values that may not be correct.|
|Force|SwitchParameter|False|When the switch IncludeOneDriveSites is used, this switch ignores the question shown that the command can take a long time to execute|
|IncludeOneDriveSites|SwitchParameter|False|By default, the OneDrives are not returned. This switch includes all OneDrives. This can take some extra time to run|
|Url|String|False|The URL of the site|
##Examples

###Example 1
```powershell
PS:> Get-SPOTenantSite
```
Returns all site collections

###Example 2
```powershell
PS:> Get-SPOTenantSite -Url http://tenant.sharepoint.com/sites/projects
```
Returns information about the project site.

###Example 3
```powershell
PS:> Get-SPOTenantSite -Detailed
```
Returns all sites with the full details of these sites

###Example 4
```powershell
PS:> Get-SPOTenantSite -IncludeOneDriveSites
```
Returns all sites including all OneDrive 4 Business sites
