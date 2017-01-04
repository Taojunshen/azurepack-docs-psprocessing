---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 37B601F3-7862-4A95-9344-D01D9392A9AE
online version: http://go.microsoft.com/fwlink/?LinkID=306484
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcNotificationSubscriber.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcNotificationSubscriber.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcNotificationSubscriber.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcNotificationSubscriber

## SYNOPSIS
Gets a notification subscriber.

## SYNTAX

### ConnectionParameters (Default)
```
Get-MgmtSvcNotificationSubscriber [[-Name] <String[]>] [-EncryptionKey <String>]
 [-EncryptionAlgorithm <String>] [-Database <String>] [-Server <String>] [-UserName <String>]
 [-Password <String>] [<CommonParameters>]
```

### ConnectionString
```
Get-MgmtSvcNotificationSubscriber [[-Name] <String[]>] [-EncryptionKey <String>]
 [-EncryptionAlgorithm <String>] [-ConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcNotificationSubscriber** cmdlet gets one or more notification subscribers from the usage service.
By default, all notification subscribers are returned.
To get a specific notification subscriber, you can provide its name.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

This cmdlet also assumes that the usage service is installed on the local computer.
If the usage service is installed on another computer, you must use the *EncryptionKey* and *EncryptionAlgorithm* parameters.

## EXAMPLES

### Example 1: Get a notification subscriber
```
PS C:\> Get-MgmtSvcNotificationSubscriber -Name "Billing"
```

This command gets the notification subscriber named Billing.
In this example, the database is on the local computer, therefore, the command does not specify the server, database, user name, or password parameters.

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

### -EncryptionAlgorithm
Specifies an encryption algorithm.

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

### -EncryptionKey
Specifies an encryption key, as a hexadecimal string.

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

### -Name
Specifies an array of notification subscriber names.
You can use wildcards.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Remove-MgmtSvcNotificationSubscriber](xref:Configuration/v1.0/Remove-MgmtSvcNotificationSubscriber.md)

[Set-MgmtSvcNotificationSubscriber](xref:Configuration/v1.0/Set-MgmtSvcNotificationSubscriber.md)


