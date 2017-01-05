---
external help file: Microsoft.WindowsAzure.MySql.PowerShell.dll-Help.xml
ms.assetid: BAF466DB-34A9-40F6-A98D-936C33C6B654
online version: http://go.microsoft.com/fwlink/?LinkID=321826
schema: 2.0.0
updated_at: 1/4/2017 6:34 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Remove-MgmtSvcMySqlServerGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Remove-MgmtSvcMySqlServerGroup.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9ea7de3be93c45294ed2319f140bd6d622b027db/AzurePack-cmdlets/MySQL/v1.0/Remove-MgmtSvcMySqlServerGroup.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-MgmtSvcMySqlServerGroup

## SYNOPSIS
Removes a MySQL server group from Windows Azure Pack.

## SYNTAX

```
Remove-MgmtSvcMySqlServerGroup [-ServerGroupId] <String> [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MgmtSvcMySqlServerGroup** removes a MySQL server group from Windows Azure Pack for Windows Server.

## EXAMPLES

### Example 1: Remove a MySQL server group
```
PS C:\> Remove-MgmtSvcMySqlServerGroup -AdminUri "https://Computer01:30004" -Token $Token -ServerGroupId "foe629"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command removes the MySQL server group with the ID foe629.

## PARAMETERS

### -AdminUri
Specifies the URI of the Windows Azure Pack administrator API.
Use the following format: https://\<computer\>:\<port\>, where \<computer\> is the computer on which the administrator API is installed.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DisableCertificateValidation
Disables certificate validation for the Windows Azure Pack installation.

If you specify this parameter, you can use self-signed certificates.

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

### -ServerGroupId
Specifies the ID of a MySQL server group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Token
Specifies an identity token.
To create a token, use the **Get-MgmtSvcToken** cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

[Add-MgmtSvcMySqlServerGroup](xref:MySQL/v1.0/Add-MgmtSvcMySqlServerGroup.md)


