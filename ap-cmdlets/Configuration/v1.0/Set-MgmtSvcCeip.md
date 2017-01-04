---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 5331A2D3-7FA5-4A83-A444-45872998A5C7
online version: http://go.microsoft.com/fwlink/?LinkID=320110
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcCeip.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcCeip.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcCeip.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcCeip

## SYNOPSIS
Updates CEIP settings for the local computer.

## SYNTAX

```
Set-MgmtSvcCeip [-EnableCeip <EnableCeip>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcCeip** cmdlet updates the Customer Experience Improvement Program (CEIP) settings for the local computer.

**NOTE:** You must run this cmdlet in a Windows PowerShell session that you have run as Administrator.

## EXAMPLES

### Example 1: Enable participation in CEIP
```
PS C:\> Set-MgmtSvcCeip -EnableCeip Yes
```

This command enables participation in CEIP.

## PARAMETERS

### -EnableCeip
Enables, when set to Yes, participation in CEIP.
To disable participation in CEIP, set this value to No.

```yaml
Type: EnableCeip
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
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

