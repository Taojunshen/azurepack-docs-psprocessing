---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 23E29EB6-DA8D-4CE1-9FD8-A23A342D8DDB
online version: http://go.microsoft.com/fwlink/?LinkID=306485
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcNotificationSubscriber.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcNotificationSubscriber.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcNotificationSubscriber.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-MgmtSvcNotificationSubscriber

## SYNOPSIS
Removes a notification subscriber.

## SYNTAX

### ConnectionParameters (Default)
```
Remove-MgmtSvcNotificationSubscriber [[-Name] <String>] [-Database <String>] [-Server <String>]
 [-UserName <String>] [-Password <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ConnectionString
```
Remove-MgmtSvcNotificationSubscriber [[-Name] <String>] [-ConnectionString <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MgmtSvcNotificationSubscriber** cmdlet removes a notification subscriber from the database.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

## EXAMPLES

### Example 1: Remove a notification subscriber
```
PS C:\> Remove-MgmtSvcNotificationSubscriber -Name "Billing"
```

This command removes the notification subscriber named Billing from the usage service.

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

### -Name
Specifies the name of a notification subscriber.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

[Get-MgmtSvcNotificationSubscriber](xref:Configuration/v1.0/Get-MgmtSvcNotificationSubscriber.md)

[Set-MgmtSvcNotificationSubscriber](xref:Configuration/v1.0/Set-MgmtSvcNotificationSubscriber.md)


