---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: A2B9B7C0-CB3E-4E62-B541-FA9AE282D05D
online version: http://go.microsoft.com/fwlink/?LinkID=321813
schema: 2.0.0
updated_at: 1/3/2017 10:42 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlServerGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlServerGroup.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/eb7bff1251dc2a22eafa120c35cbbc43529d3762/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlServerGroup.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcSqlServerGroup

## SYNOPSIS
Gets a SQL Server group.

## SYNTAX

```
Get-MgmtSvcSqlServerGroup [[-GroupName] <String[]>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcSqlServerGroup** cmdlet gets SQL Server groups.
By default, all SQL Server groups are returned.
To get a specific server group, use the *GroupName* parameter.

## EXAMPLES

### Example 1: Get a specific SQL server group
```
PS C:\> Get-MgmtSvcSqlServerGroup -AdminUri "https://Computer01:30004" -Token $Token -GroupName "SQL Group 01"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets the SQL Server group named SQL Group 01.

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
Specifies an array of SQL Server group names.

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

### None

## OUTPUTS

### SqlServerGroup
This cmdlet emits a **SqlServerGroup** object.

## NOTES

## RELATED LINKS

[Add-MgmtSvcSqlServerGroup](xref:SQLServer/v1.0/Add-MgmtSvcSqlServerGroup.md)

[Remove-MgmtSvcSqlServerGroup](xref:SQLServer/v1.0/Remove-MgmtSvcSqlServerGroup.md)


