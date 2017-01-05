---
external help file: Microsoft.WindowsAzure.MySql.PowerShell.dll-Help.xml
ms.assetid: 42223C47-D76E-4EC4-9D37-935F82572576
online version: http://go.microsoft.com/fwlink/?LinkID=321824
schema: 2.0.0
updated_at: 1/4/2017 6:34 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlServerGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlServerGroup.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9ea7de3be93c45294ed2319f140bd6d622b027db/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlServerGroup.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcMySqlServerGroup

## SYNOPSIS
Gets a MySQL server group.

## SYNTAX

```
Get-MgmtSvcMySqlServerGroup [[-GroupName] <String[]>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcMySqlServerGroup** cmdlet gets MySQL server groups.
By default, all MySQL server groups are returned.
To get a specific MySQL server group, use the *GroupName* parameter.

## EXAMPLES

### Example 1: Get a specific MySQL server group
```
PS C:\> Get-MgmtSvcMySqlServerGroup -AdminUri "https://Computer01:30004" -Token $Token -GroupName "MySQL Group 01"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets the MySQL server group named MySQL Group 01.

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

### -GroupName
Specifies an array of MySQL server group names.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-MgmtSvcMySqlServerGroup](xref:MySQL/v1.0/Add-MgmtSvcMySqlServerGroup.md)

[Remove-MgmtSvcMySqlServerGroup](xref:MySQL/v1.0/Remove-MgmtSvcMySqlServerGroup.md)


