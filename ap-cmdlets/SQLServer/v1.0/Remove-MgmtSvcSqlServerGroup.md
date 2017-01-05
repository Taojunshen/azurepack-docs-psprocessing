---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: 6165B8FD-AEF9-4FE0-B725-50A5756A8B50
online version: http://go.microsoft.com/fwlink/?LinkID=321815
schema: 2.0.0
updated_at: 1/3/2017 10:42 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Remove-MgmtSvcSqlServerGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Remove-MgmtSvcSqlServerGroup.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/eb7bff1251dc2a22eafa120c35cbbc43529d3762/AzurePack-cmdlets/SQLServer/v1.0/Remove-MgmtSvcSqlServerGroup.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-MgmtSvcSqlServerGroup

## SYNOPSIS
Removes a SQL Server group from Windows Azure Pack.

## SYNTAX

```
Remove-MgmtSvcSqlServerGroup [-ServerGroupId] <String> [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MgmtSvcSqlServerGroup** cmdlet removes a SQL Server group from Windows Azure Pack for Windows Server.

## EXAMPLES

### Example 1: Remove a SQL Server groups
```
PS C:\> Remove-MgmtSvcSqlServerGroup -AdminUri "https://Computer01:30004" -Token $Token -ServerGroupId "g5sho0"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command removes the SQL Server group with the ID g5sho0.

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

### -ServerGroupId
Specifies the ID of a SQL Server group.

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### ServerGroupId
You can pipe a **ServerGroupId** object to this cmdlet.

## OUTPUTS

### Boolean
This cmdlet emits a **Boolean** object that indicates success or failure.

## NOTES

## RELATED LINKS

[Add-MgmtSvcSqlServerGroup](xref:SQLServer/v1.0/Add-MgmtSvcSqlServerGroup.md)

[Get-MgmtSvcSqlServerGroup](xref:SQLServer/v1.0/Get-MgmtSvcSqlServerGroup.md)


