---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: A37E2BAA-2025-4C94-B5BC-F6934DF6B937
online version: http://go.microsoft.com/fwlink/?LinkID=296534
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcDatabaseUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcDatabaseUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcDatabaseUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcDatabaseUser

## SYNOPSIS
Adds SQL authentication credentials for a user to the database.

## SYNTAX

```
Add-MgmtSvcDatabaseUser -User <String> -UserPassword <String> [-RoleName <String>] [-Force] -Schema <String>
 [-ConnectionString <String>] [-Server <String>] [-Database <String>] [-UserName <String>] [-Password <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcDatabaseUser** cmdlet adds SQL authentication credentials for a specified user in the database.
Specify the user name and password.
You can also specify a user role for the account.
Note that the **Initialize-MgmtSvcFeature** cmdlet adds the necessary users to Windows Azure Pack for Windows Server.
You only need to use **Add-MgmtSvcDatabaseUser** to add additional users.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

## EXAMPLES

### Example 1: Add a user to a database for a schema
```
PS C:\> Add-MgmtSvcDatabaseUser -Schema "SqlServer" -User "user" -UserPassword "Sand3289" -RoleName "DBO" -Database "Contoso.MgmtSvc.Store" -Server "ContosoSQLServer"
```

This command adds the user named user to the database named Contoso.MgmtSvc.Store for the schema SqlServer.
The command specifies the computer that runs SQL Server.
The command also specifies a password and the role DBO for the new user.

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

### -Force
{{Fill Force Description}}

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

### -RoleName
Specifies the name of a role for the added account.
Roles are used to grant or deny user access to database objects.
Roles and database access are specific to a schema.

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
Specifies the user name of the principal.
The cmdlet adds this account to the database for the specified schema.

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

### -UserPassword
Specifies a password for the principal account specified by the *User* parameter.
The cmdlet adds this account to the database for the specified schema.

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

[Remove-MgmtSvcDatabaseUser](xref:Configuration/v1.0/Remove-MgmtSvcDatabaseUser.md)

[Set-MgmtSvcDatabaseUser](xref:Configuration/v1.0/Set-MgmtSvcDatabaseUser.md)

[Get-MgmtSvcSchema](xref:Configuration/v1.0/Get-MgmtSvcSchema.md)

[Install-MgmtSvcDatabase](xref:Configuration/v1.0/Install-MgmtSvcDatabase.md)


