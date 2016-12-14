---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: BE94455C-1DCA-48B6-BE37-88B4E43C4ADB
online version: http://go.microsoft.com/fwlink/?LinkID=321808
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/SQLServer/v1.0/Add-MgmtSvcSqlServerGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/SQLServer/v1.0/Add-MgmtSvcSqlServerGroup.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/SQLServer/v1.0/Add-MgmtSvcSqlServerGroup.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcSqlServerGroup

## SYNOPSIS
Adds a SQL Server group to Windows Azure Pack.

## SYNTAX

### ByProperties (Default)
```
Add-MgmtSvcSqlServerGroup [-GroupName] <String> [-ResourceGovernorEnabled] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject
```
Add-MgmtSvcSqlServerGroup [[-ServerGroup] <SqlServerGroup>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcSqlServerGroup** adds a SQL Server group to Windows Azure Pack for Windows Server.

## EXAMPLES

### Example 1: Add a SQL Server group
```
PS C:\>Add-MgmtSvcSqlServerGroup -AdminUri "https://Computer01:30004" -Token $Token -GroupName "SQL Group 01"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This example adds a SQL Server group named SQL Group 01.

## PARAMETERS

### -AdminUri
Specifies the URI of the Windows Azure Pack administrator API.
Use the following format: https://\< computer\>:\<port\>, where \<computer\> is the computer on which the administrator API is installed.

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
Default value: None
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

### -GroupName
Specifies a name for the SQL Server group.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGovernorEnabled
Indicates that the server group has the resource governor enabled.

```yaml
Type: SwitchParameter
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerGroup
Specifies a SQL Server group object.

```yaml
Type: SqlServerGroup
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
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
Shows what would happen if the cmdlet runs. The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### SqlServerGroup
You can pipe a **SqlServerGroup** object to this cmdlet.

## OUTPUTS

### SqlServerGroup
This cmdlet emits a **SqlServerGroup** object.

## NOTES

## RELATED LINKS

[Get-MgmtSvcSqlServerGroup](xref:SQLServer/v1.0/Get-MgmtSvcSqlServerGroup.md)

[Remove-MgmtSvcSqlServerGroup](xref:SQLServer/v1.0/Remove-MgmtSvcSqlServerGroup.md)


