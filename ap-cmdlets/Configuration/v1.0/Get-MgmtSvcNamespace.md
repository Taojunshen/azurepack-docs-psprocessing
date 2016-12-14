---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 91CC74DD-5FCA-4872-B8E7-0A10BDE54B58
online version: http://go.microsoft.com/fwlink/?LinkID=296540
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcNamespace.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcNamespace.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcNamespace.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcNamespace

## SYNOPSIS
Gets registered management service namespaces.

## SYNTAX

```
Get-MgmtSvcNamespace [[-Namespace] <String[]>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcNamespace** cmdlet returns a list of registered management service namespaces.
A namespace groups a set of related configuration settings.
For example, a set of connectionStrings andApp settings in the web.config file of a feature constitutes a namespace.

## EXAMPLES

### Example 1: Get management service namespaces
```
PS C:\>Get-MgmtSvcNamespace
MySQL
SQLServer
Monitoring
UsageService
UsageCollector
WebAppGallery
Notification
AdminAPI
TenantAPI
TenantPublicAPI
AdminSite
TenantSite
```

This command gets the management service namespaces for the local computer.

## PARAMETERS

### -Namespace
Specifies an array of namespaces of management service settings.

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

[Get-MgmtSvcEndpoint](xref:Configuration/v1.0/Get-MgmtSvcEndpoint.md)

[Get-MgmtSvcSchema](xref:Configuration/v1.0/Get-MgmtSvcSchema.md)


