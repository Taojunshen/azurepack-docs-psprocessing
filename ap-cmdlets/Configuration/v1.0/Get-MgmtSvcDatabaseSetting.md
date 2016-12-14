---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 5A39C1FA-C245-411F-9B2A-17361AE2E91C
online version: http://go.microsoft.com/fwlink/?LinkID=296537
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcDatabaseSetting.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcDatabaseSetting.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcDatabaseSetting.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcDatabaseSetting

## SYNOPSIS
Reads settings from a configuration database.

## SYNTAX

### ConnectionParameters (Default)
```
Get-MgmtSvcDatabaseSetting [[-Namespace] <String[]>] [[-Name] <String[]>] [-Passphrase <String>]
 [-Database <String>] [-Server <String>] [-UserName <String>] [-Password <String>] [<CommonParameters>]
```

### ConnectionString
```
Get-MgmtSvcDatabaseSetting [[-Namespace] <String[]>] [[-Name] <String[]>] [-Passphrase <String>]
 [-ConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcDatabaseSetting** cmdlet reads the configuration settings of a management service component from the database.
A setting consists of a namespace, a name, and a value.
If you protected a setting by encrypting it, you need to supply a value for the Passphrase parameter to decrypt the setting.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

## EXAMPLES

### Example 1: Get a setting
```
PS C:\>$ConnectionString = 'Data Source=rd-source04;Initial Catalog=Microsoft.MgmtSvc.Config;User ID=SA;Password=PassWord01'
PS C:\> Get-MgmtSvcDatabaseSetting -Namespace "TenantSite" -Name "machineKey.decryptionKey" -ConnectionString $ConnectionString -Passphrase "PassPhrase01"
```

The first command stores a connection string in the $ConnectionString variable.

The second command gets the setting that has the specified namespace, name, and value.
A passphrase is supplied to decrypt the setting.

## PARAMETERS

### -ConnectionString
Specifies an SQL connection string.

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Specifies a database name.
The Config schema must be in stalled in this database.

By default, the Config schema is installed in the following databases:

- Microsoft.MgmtSvc.Config
-- Microsoft.MgmtSvc.PortalConfigStore
- Microsoft.MgmtSvc.Store

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names for a setting.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Specifies an array of namespaces for a setting.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Passphrase
Specifies a passphrase.
If a setting was previously encrypted, provide a passphrase to decrypt the setting.
A passphrase must be provided if the setting requires it.

By default, only Microsoft.MgmtSvc.Config settings require a passphrase.

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
Specifies a password for the user to connect to the database.

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
Specifies the name of the computer on which the SQL database resides.

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the name of a user account used to connect to the database.

```yaml
Type: String
Parameter Sets: ConnectionParameters
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

[Set-MgmtSvcDatabaseSetting](xref:Configuration/v1.0/Set-MgmtSvcDatabaseSetting.md)

[Test-MgmtSvcPassphrase](xref:Configuration/v1.0/Test-MgmtSvcPassphrase.md)

[Reset-MgmtSvcPassphrase](xref:Configuration/v1.0/Reset-MgmtSvcPassphrase.md)

[Get-MgmtSvcDefaultDatabaseName](xref:Configuration/v1.0/Get-MgmtSvcDefaultDatabaseName.md)


