---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 5492B41D-7A02-4FC5-B868-238F5A3FD2E4
online version: http://go.microsoft.com/fwlink/?LinkID=296550
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Protect-MgmtSvcConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Protect-MgmtSvcConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Protect-MgmtSvcConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Protect-MgmtSvcConfiguration

## SYNOPSIS
Encrypts sections of the web.config file for a namespace.

## SYNTAX

```
Protect-MgmtSvcConfiguration [-Namespace] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Protect-MgmtSvcConfiguration** cmdlet encrypts sections of the web.config file for a specified namespace.
The cmdlet encrypts the sections of the web.config file that contain secrets, such as connectionStrings, appSettings, and machineKey.
To access these settings, use the passphrase parameters described in the **Get-MgmtSvcSetting** and **Set-MgmtSvcSetting** cmdlets.
However, you do not need to access the settings by using the cmdlets to unprotect the configuration.
This is only necessary to access the web.config file in an editor.

Run this cmdlet on the computer that hosts the web.config file.

## EXAMPLES

### Example 1: Encrypt the config.web file for a namespace
```
PS C:\>Protect-MgmtSvcConfiguration -Namespace "AdminSite"
```

This command encrypts the sections of the web.config file that contains secrets, such as connectionStrings, appSettings, and machineKey, for the namespace AdminSite.

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

[Unprotect-MgmtSvcConfiguration](xref:Configuration/v1.0/Unprotect-MgmtSvcConfiguration.md)

[Test-MgmtSvcProtectedConfiguration](xref:Configuration/v1.0/Test-MgmtSvcProtectedConfiguration.md)

[Get-MgmtSvcSetting](xref:Configuration/v1.0/Get-MgmtSvcSetting.md)

[Set-MgmtSvcSetting](xref:Configuration/v1.0/Set-MgmtSvcSetting.md)


