---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: A737AEF7-127B-41EB-A2CD-F82018F85C12
online version: http://go.microsoft.com/fwlink/?LinkID=320112
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Test-MgmtSvcProtectedConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Test-MgmtSvcProtectedConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Test-MgmtSvcProtectedConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Test-MgmtSvcProtectedConfiguration

## SYNOPSIS
Tests whether a configuration is protected.

## SYNTAX

```
Test-MgmtSvcProtectedConfiguration [-Namespace] <String> [<CommonParameters>]
```

## DESCRIPTION
The **Test-MgmtSvcProtectedConfiguration** cmdlet tests whether the sections of the Web.config file that contain secrets are protected.
If the configuration for the namespace is protected, a value of True is returned.
If the configuration is not protected, a value of False is returned.
The cmdlet displays a warning if the configuration is not protected.

It is recommended that you keep your Web.config file protected.
To protect a configuration, use the **Protect-MgmtSvcConfiguration** cmdlet.
You can unprotect your configuration to update the Web.config file by using the **Unprotect-MgmtSvcConfiguration**.
However, you should then return the configuration to a protected state.

## EXAMPLES

### Example 1: Test a protectected configuration
```
PS C:\> Test-MgmtSvcProtectedConfiguration -Namespace "AdminSite"
```

This command tests the protected configuration for the namespace AdminSite.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Protect-MgmtSvcConfiguration](xref:Configuration/v1.0/Protect-MgmtSvcConfiguration.md)

[Unprotect-MgmtSvcConfiguration](xref:Configuration/v1.0/Unprotect-MgmtSvcConfiguration.md)


