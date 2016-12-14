---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: B5A810E4-AFDC-4FA5-BEC1-5F7F69554EBB
online version: http://go.microsoft.com/fwlink/?LinkID=296538
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcEndpoint.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcEndpoint.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcEndpoint.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcEndpoint

## SYNOPSIS
Gets management service component endpoints.

## SYNTAX

```
Get-MgmtSvcEndpoint [[-Namespace] <String[]>] [[-Name] <String[]>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcEndpoint** cmdlet gets one or more management service component endpoints.

You must run this cmdlet on the computer that hosts the desired namespace.

## EXAMPLES

### Example 1: Get management service component endpoints
```
PS C:\>Get-MgmtSvcEndpoint -Namespace "AdminAPI"
```

This command gets endpoints that are configured for the feature in the namespace named AdminAPI.

## PARAMETERS

### -Name
Specifies an array of endpoint names.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Specifies an array of endpoint namespaces.

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

[Get-MgmtSvcSchema](xref:Configuration/v1.0/Get-MgmtSvcSchema.md)


