---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 0F00DC11-4F4C-4A0B-99AF-9A2D64D65BC3
online version: http://go.microsoft.com/fwlink/?LinkID=296546
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Install-MgmtSvcDatabase.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Install-MgmtSvcDatabase.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Install-MgmtSvcDatabase.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Install-MgmtSvcDatabase

## SYNOPSIS
Creates a schema and database objects in a database.

## SYNTAX

```
Install-MgmtSvcDatabase -Schema <String> [-ConnectionString <String>] [-Server <String>] [-Database <String>]
 [-UserName <String>] [-Password <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Install-MgmtSvcDatabase** cmdlet creates schema and associated database objects.
The cmdlet creates the database if it does not already exist.
The cmdlet installs a database schema on the specific server from scripts consumed during portal installation.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

You can run this cmdlet repeatedly on the existing database without destroying data.
You can specify a new or an existing database, and, depending on the schemas, you can install multiple schemas in the same database.

The **Initialize-MgmtSvcFeature** cmdlet calls this cmdlet to configure the required databases.

After importing the latest commands (**Import-Module -Name MgmtSvcConfig**), you can run **Install-MgmtSvcDatabase** to upgrade specific database schemas (specified by the schema parameter).
For example: **Install-MgmtSvcDatabase -Schema SqlServer -Server "$env:ComputerName" -UserName "sysadmin_login" -Password "sysadmin_password"**.

Once you do this, you'll be using the latest version of the installation database, which provides bug fixes and support for new features.
For example, using Windows Authentication when creating databases in SQL Server, only works after you've upgraded your database schema.Since the installer can't upgrade your database automatically, you must manually run the upgrade script and provide system administrator credentials to the SQL Server that hosts your management databases (*UserName* and *Password*).

For your installation to support all features of the latest release, you must perform appropriate backups and manually upgrade you installation by running Import-Module -Name MgmtSvcConfig ; Install-MgmtSvcDatabase -Schema SqlServer -Server "$env:ComputerName" -UserName "sysadmin_login" -Password "sysadmin_password".

## EXAMPLES

### Example 1: Add a schema to the database
```
PS C:\>Install-MgmtSvcDatabase -Schema "Management" -ConnectionString ""Data Source=$env:ComputerName;Initial Catalog=Management;Integrated Security=SSPI""
```

This command adds the schema Management to the database.

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
The cmdlet installs this schema.

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

[Test-MgmtSvcDatabase](xref:Configuration/v1.0/Test-MgmtSvcDatabase.md)

[Uninstall-MgmtSvcDatabase](xref:Configuration/v1.0/Uninstall-MgmtSvcDatabase.md)


