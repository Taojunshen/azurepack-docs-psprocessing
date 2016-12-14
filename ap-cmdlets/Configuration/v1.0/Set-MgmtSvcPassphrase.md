---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 8BED1F5B-E269-476C-A9DA-9874C88977D0
online version: http://go.microsoft.com/fwlink/?LinkID=320111
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcPassphrase.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcPassphrase.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcPassphrase.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcPassphrase

## SYNOPSIS
Sets the passphrase for a configuration database.

## SYNTAX

### ConnectionParameters (Default)
```
Set-MgmtSvcPassphrase -Passphrase <String> [-Database <String>] [-Server <String>] [-UserName <String>]
 [-Password <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ConnectionString
```
Set-MgmtSvcPassphrase -Passphrase <String> [-ConnectionString <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcPassphrase** cmdlet sets the passphrase that the management service uses to encrypt sensitive data in the configuration database.

A passphrase can only be set once.
To replace the passphrase, use the **Reset-MgmtSvcPassPhrase** cmdlet.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

## EXAMPLES

### Example 1: Set a passphrase
```
PS C:\>Set-MgmtSvcPassphrase -Server "Contoso01" -UserName "sa" -Password '********' -Passphrase '*********'
```

This command sets the passphrase for the configuration store on the computer named Contoso01.

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

### -Passphrase
Specifies a passphrase.

The passphrase must contain at least eight characters and contain at least one non-alphanumeric character.
Remember to protect the passphrase.
You cannot recover the passphrase.

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

[Reset-MgmtSvcPassphrase](xref:Configuration/v1.0/Reset-MgmtSvcPassphrase.md)

[Test-MgmtSvcPassphrase](xref:Configuration/v1.0/Test-MgmtSvcPassphrase.md)


