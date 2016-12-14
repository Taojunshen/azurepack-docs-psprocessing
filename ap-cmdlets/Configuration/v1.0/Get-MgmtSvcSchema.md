---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: FE732E79-2E2C-411D-8B3F-5A5D50DF6903
online version: http://go.microsoft.com/fwlink/?LinkID=296541
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcSchema.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcSchema.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcSchema.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcSchema

## SYNOPSIS
Gets registered schemas.

## SYNTAX

```
Get-MgmtSvcSchema [[-Schema] <String[]>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcSchema** cmdlet returns a list of registered management service schemas.
A schema groups a set of related SQL scripts.
A schema represents the database objects that a resource provider uses or that are shared by features.

## EXAMPLES

### Example 1: Get all registered schemas
```
PS C:\>Get-MgmtSvcSchema

MySQL
SQLServer
Usage
WebAppGallery
Notification
Management
Config
PortalAspNet
PortalNotification
```

This command gets all of the management service schemas that are registered on the local computer.

## PARAMETERS

### -Schema
Specifies an array of component schemas.
You can use wildcards.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MgmtSvcFeature](xref:Configuration/v1.0/Get-MgmtSvcFeature.md)

[Get-MgmtSvcNamespace](xref:Configuration/v1.0/Get-MgmtSvcNamespace.md)

[Get-MgmtSvcEndpoint](xref:Configuration/v1.0/Get-MgmtSvcEndpoint.md)

[Remove-MgmtSvcDatabaseUser](xref:Configuration/v1.0/Remove-MgmtSvcDatabaseUser.md)

[Install-MgmtSvcDatabase](xref:Configuration/v1.0/Install-MgmtSvcDatabase.md)

[Add-MgmtSvcDatabaseUser](xref:Configuration/v1.0/Add-MgmtSvcDatabaseUser.md)

[Set-MgmtSvcDatabaseUser](xref:Configuration/v1.0/Set-MgmtSvcDatabaseUser.md)

[Test-MgmtSvcDatabase](xref:Configuration/v1.0/Test-MgmtSvcDatabase.md)


