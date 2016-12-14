---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 697B480C-F0CC-4825-8B21-96C2A9EEE462
online version: http://go.microsoft.com/fwlink/?LinkID=296559
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Test-MgmtSvcDatabase.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Test-MgmtSvcDatabase.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Test-MgmtSvcDatabase.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Test-MgmtSvcDatabase

## SYNOPSIS
Verifies database installation.

## SYNTAX

```
Test-MgmtSvcDatabase -Schema <String> [-ConnectionString <String>] [-Server <String>] [-Database <String>]
 [-UserName <String>] [-Password <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Test-MgmtSvcDatabase** cmdlet verifies installation of a management service database.
The cmdlet returns the version of the installed schema.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

## EXAMPLES

### Example 1: Verify a schema installation
```
PS C:\>Test-MgmtSvcDatabase -Schema "Config" -ConnectionString 'Data Source=mysqlserver;Initial Catalog=Microsoft.MgmtSvc.Config;User ID=SysAdmin;Password=Zoom2345'
```

This command verifies that the schema named Config is installed.

## PARAMETERS

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
The cmdlet verifies installation of this schema.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Install-MgmtSvcDatabase](xref:Configuration/v1.0/Install-MgmtSvcDatabase.md)

[Uninstall-MgmtSvcDatabase](xref:Configuration/v1.0/Uninstall-MgmtSvcDatabase.md)


