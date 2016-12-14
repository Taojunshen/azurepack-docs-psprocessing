---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: B35B2780-FB2A-4644-ACFE-5AEA3BA1A792
online version: http://go.microsoft.com/fwlink/?LinkID=321241
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Initialize-WebSitesInstance.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Initialize-WebSitesInstance.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Initialize-WebSitesInstance.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Initialize-WebSitesInstance

## SYNOPSIS
Creates and configures a website.

## SYNTAX

```
Initialize-WebSitesInstance [[-Settings] <Hashtable>] [-Force] [<CommonParameters>]
```

## DESCRIPTION
The **Initialize-WebSitesInstance** cmdlet creates and configures a website.
Configuration information comes from a user-created hash table: a data structure containing property names and their associated values.

## EXAMPLES

### Example 1: Create and configure a website
```
PS C:\> $ControllerInitializationSettings = @{ hosting = "Server=CN-SERVER;Initial Catalog=Hosting;User ID=sa;Password=Password01!"; resourceMetering = "Server=CN-SERVER;Initial Catalog=ResourceMetering;User ID=sa;Password=Password01!"; managementServerAdminUserName = "{0}\Admin"; managementServerAdminPassword = "Password01!"; fileServerAdminUserName = "{0}\Admin"; fileServerAdminPassword = "Password01!"; frontEndAdminUserName = "{0}\Admin"; frontEndAdminPassword = "Password01!"; publisherAdminUserName = "{0}\Admin"; publisherAdminPassword = "Password01!"; workerAdminUserName = "{0}\Admin"; workerAdminPassword = "Password01!"; adminUserName = "{0}\RestMwhImpersonation"; adminPassword = "Password01!"; dnsSuffix = "test.com"; managementServerName = "MN-SERVER"; fileServerName = "FS-SERVER"; fileServerType = "WindowsSingle"; fileShareOwnerUserName = "FileShareOwner"; fileShareOwnerPassword = "Password01!"; fileShareUserUserName = "FileShareUser"; fileShareUserPassword = "Password01!"; cloudAdminUserName = "administrator"; cloudAdminPassword = "Password01!"; centralCertStoreUserName = "Certificateshareuser"; centralCertStorePassword = "Password01!"; contentShareUNCPath = "\\FS-SERVER\Websites"; contentShareLocalPath = "C:\Websites"; certificateShareUNCPath = "\\FSSERVER01\Certificates"; certificateShareLocalPath = "C:\Certificates"; feedUrl = "http://FeedURL/feeds/List.xml"; customFeeds = "http://FeedURL/Products.xml"; SQMEnabled = "False"; MicrosoftUpdateEnabled = "True" }
PS C:\> Initialize-WebSitesInstance -Settings $ControllerInitializationSettings -Verbose
```

These two commands create a website by using the **Initialize-WebSitesInstance** cmdlet.
The first command in the example creates a hash table containing the configuration values for the new site.
This hash table is stored in the variable $ControllerInitializationSettings.

The second command then uses $ControllerInitializationSettings and the **Initialize-WebSitesInstance** cmdlet to create and configure the new website.

## PARAMETERS

### -Force
{{Fill Force Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Settings
Specifies a hash table containing configuration information for the new website.
Each entry in the hash table consist of a property name followed by an equals sign, followed by the property value, For example, this syntax contains a single property (hosting):

`@{hosting = "Server=CN-SERVER;Initial Catalog=Hosting;User ID=sa;Password=Password01!"}`

Multiple properties are specified by using semicons to separate individual entries.
For example, this syntax contains two properties (hosting and fileServerType) :

`@{hosting = "Server=CN-SERVER;Initial Catalog=Hosting;User ID=sa;Password=Password01!"; fileServerType = "WindowsSingle" }`

See https://technet.microsoft.com/en-us/library/dn554319.aspxhttps://technet.microsoft.com/en-us/library/dn554319.aspx for more examples.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

