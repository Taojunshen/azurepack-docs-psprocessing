---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: EC158CAD-DE0E-4C01-9734-E6348F7A7832
online version: http://go.microsoft.com/fwlink/?LinkID=296555
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcDatabaseSetting.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcDatabaseSetting.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcDatabaseSetting.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcDatabaseSetting

## SYNOPSIS
Writes settings to the configuration database.

## SYNTAX

### ConnectionParameters (Default)
```
Set-MgmtSvcDatabaseSetting [-Namespace] <String> [-Name] <String> [[-Value] <String>] [-Force]
 [-Passphrase <String>] [-Database <String>] [-Server <String>] [-UserName <String>] [-Password <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ConnectionString
```
Set-MgmtSvcDatabaseSetting [-Namespace] <String> [-Name] <String> [[-Value] <String>] [-Force]
 [-Passphrase <String>] [-ConnectionString <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcDatabaseSetting** cmdlet writes configuration settings for a management service component to the database.
A setting consists of a namespace, a name, and a value.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

## EXAMPLES

### Example 1: Write a setting to the database
```
PS C:\>$MK = New-MgmtSvcMachineKey
PS C:\> $ConnectionString = 'Data Source=mysqlserver;Initial Catalog=Microsoft.MgmtSvc.Config;User ID=sa;Password=Book67pp'
PS C:\> Set-MgmtSvcDatabaseSetting -ConnectionString $ConnectionString -Namespace "TenantSite" -Name "machineKey.decryptionKey" -Value $MK.Attributes(""decryptionKey"").Value -Force -Passphrase "PassPhrase01!"
```

The first command creates a machine key by using the **New-MgmtSvcMachineKey** cmdlet, and stores it in the $MK variable.

The second command stores a connection string in the $ConnectionString  variable.

The last command writes the namespace, name, and value to the database.
The command uses the connection string stored in $ConnectionString and the machine key stored in $MK.
The command also includes a passphrase.

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

### -Force
Performs the action without a confirmation message.

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

### -Name
Specifies the name of a setting.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Specifies the namespace of a setting.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Passphrase
Specifies a passphrase.
The database encrypts items in the configuration store by using this passphrase.

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
Specifies the name of a user account.

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

### -Value
Specifies the value of a setting.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

[Get-MgmtSvcDatabaseSetting](xref:Configuration/v1.0/Get-MgmtSvcDatabaseSetting.md)

[Test-MgmtSvcPassphrase](xref:Configuration/v1.0/Test-MgmtSvcPassphrase.md)

[Reset-MgmtSvcPassphrase](xref:Configuration/v1.0/Reset-MgmtSvcPassphrase.md)

[New-MgmtSvcMachineKey](xref:Configuration/v1.0/New-MgmtSvcMachineKey.md)


