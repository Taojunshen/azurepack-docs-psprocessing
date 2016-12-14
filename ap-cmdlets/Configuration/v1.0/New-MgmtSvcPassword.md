---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: D87B5C19-3F9D-4C7B-ACAE-D6503B2276F1
online version: http://go.microsoft.com/fwlink/?LinkID=296548
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcPassword.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcPassword.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcPassword.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-MgmtSvcPassword

## SYNOPSIS
Creates a random password.

## SYNTAX

```
New-MgmtSvcPassword [-Length <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **New-MgmtSvcPassword** cmdlet generates a cryptographically strong password for use with other settings.
This cmdlet generates a value in memory.
The Initialize-MgmtSvcFeature cmdlet calls this cmdlet to generate the passwords used across Windows Azure Pack for Windows Server components.
For example, passwords used for database connection strings and access to resource providers.

Use this cmdlet to generate a cryptographically secure random password for use in setting basic authorization credentials.
You can use the returned string as the value for the *Value* parameter for the **Set-MgmtSvcSetting** cmdlet, or as the password value in a connection string.

## EXAMPLES

### Example 1: Create a password
```
PS C:\>New-MgmtSvcPassword -Length 64
```

This command creates a random password that contains 64 characters.

## PARAMETERS

### -Length
Specifies a password length.
Choose a value between 8 and 128, in multiples of 4.
The default length is 32 characters.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

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

[Set-MgmtSvcSetting](xref:Configuration/v1.0/Set-MgmtSvcSetting.md)


