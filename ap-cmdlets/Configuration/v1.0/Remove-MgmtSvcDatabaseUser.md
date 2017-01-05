---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 97AF93CA-BE1D-4E48-95F7-80007DAF3D8E
online version: http://go.microsoft.com/fwlink/?LinkID=296551
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcDatabaseUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcDatabaseUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcDatabaseUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-MgmtSvcDatabaseUser

## SYNOPSIS
Removes a principal from the database.

## SYNTAX

```
Remove-MgmtSvcDatabaseUser -User <String> -Schema <String> [-ConnectionString <String>] [-Server <String>]
 [-Database <String>] [-UserName <String>] [-Password <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MgmtSvcDatabaseUser** cmdlet removes a principal account for a specified schema from the database.
Specify the user name and schema.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

Use this cmdlet when uninstalling Windows Azure Pack for Windows Server.
When you uninstall the product, you must uninstall the databases and remove the database users.

## EXAMPLES

### Example 1: Remove a user account
```
PS C:\> Remove-MgmtSvcDatabaseUser -Schema "Usage" -User "MgmtSvc-Usage" -Database "Microsoft.MgmtSvc.Usage" -Password "PassWord!" -Server "ContosoSQLServer" -UserName "SysAdmin"
```

This command removes the user named MgmtSvc-Usage from the Usage schema in the database named Contoso.MgmtSvc.Usage.
The command specifies the computer that runs SQL server as ContosoSQLServer.
The command also specifies a user named SysAdmin, which has permissions to make this change, along with the password for that account.

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

### -ConnectionString
Specifies an SQL connection string.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Specifies a database name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Specifies a password.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schema
Specifies a schema.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
Specifies the name of the computer on which the SQL database resides.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -User
Specifies the user name of a principal.
The cmdlet removes this account from the database for the specified schema.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the name of a user account.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[Add-MgmtSvcDatabaseUser](xref:Configuration/v1.0/Add-MgmtSvcDatabaseUser.md)

[Set-MgmtSvcDatabaseUser](xref:Configuration/v1.0/Set-MgmtSvcDatabaseUser.md)


