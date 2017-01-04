---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: B9AED2F1-CE67-4D90-AD51-5A144EB853ED
online version: http://go.microsoft.com/fwlink/?LinkID=296539
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcFeature.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcFeature.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcFeature.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcFeature

## SYNOPSIS
Gets management service features.

## SYNTAX

```
Get-MgmtSvcFeature [[-Name] <String[]>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcFeature** cmdlet returns a list of installed management service features, including whether the feature has been configured.

## EXAMPLES

### Example 1: Get management service features
```
PS C:\> Get-MgmtSvcFeature
```

This command gets all management service features that are installed on the local computer.
The command also returns the configuration status of the computer.

## PARAMETERS

### -Name
Specifies an array of names of management service features.
You can use wildcards.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

[Initialize-MgmtSvcFeature](xref:Configuration/v1.0/Initialize-MgmtSvcFeature.md)

[Get-MgmtSvcEndpoint](xref:Configuration/v1.0/Get-MgmtSvcEndpoint.md)

[Get-MgmtSvcNamespace](xref:Configuration/v1.0/Get-MgmtSvcNamespace.md)

[Get-MgmtSvcSchema](xref:Configuration/v1.0/Get-MgmtSvcSchema.md)


