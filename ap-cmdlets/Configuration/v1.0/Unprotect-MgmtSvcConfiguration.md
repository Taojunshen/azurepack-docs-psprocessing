---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: B5427058-AD05-49E1-B48A-9D41E4C0B011
online version: HYPERLINK "http://go.microsoft.com/fwlink/?LinkID=296562" http://go.microsoft.com/fwlink/?LinkID=296562
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Unprotect-MgmtSvcConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Unprotect-MgmtSvcConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Unprotect-MgmtSvcConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Unprotect-MgmtSvcConfiguration

## SYNOPSIS
Decrypts sections of the web.config file for a namespace.

## SYNTAX

```
Unprotect-MgmtSvcConfiguration [-Namespace] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Unprotect-MgmtSvcConfiguration** cmdlet decrypts sections of the web.config file for a specified namespace.
The cmdlet decrypts the sections of the web.config file that contains secrets, such as connectionStrings, appSettings, and machineKey.
To encrypt these sections, use the **Protect-MgmtSvcConfiguration** cmdlet.

Run this cmdlet on the computer that hosts the web.config file.

## EXAMPLES

### Example 1: Decrypt the web.config file for a namespace
```
PS C:\> Unprotect-MgmtSvcConfiguration -Namespace "AdminSite"
```

This command decrypts the connectionStrings and appSettings sections of the web.config file for the namespace AdminSite.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Specifies a namespace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Protect-MgmtSvcConfiguration](xref:Configuration/v1.0/Protect-MgmtSvcConfiguration.md)

[Test-MgmtSvcProtectedConfiguration](xref:Configuration/v1.0/Test-MgmtSvcProtectedConfiguration.md)

[Get-MgmtSvcSetting](xref:Configuration/v1.0/Get-MgmtSvcSetting.md)

[Set-MgmtSvcSetting](xref:Configuration/v1.0/Set-MgmtSvcSetting.md)


