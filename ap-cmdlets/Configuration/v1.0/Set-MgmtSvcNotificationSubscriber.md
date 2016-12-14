---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 4AC018F4-4483-4BEB-A898-D53A6AD5C204
online version: http://go.microsoft.com/fwlink/?LinkID=306487
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcNotificationSubscriber.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcNotificationSubscriber.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcNotificationSubscriber.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcNotificationSubscriber

## SYNOPSIS
Adds or updates a notification subscriber.

## SYNTAX

### ByProperties (Default)
```
Set-MgmtSvcNotificationSubscriber -Name <String> [-Enabled <Boolean>]
 [-SubscriberType <NotificationSubscriberType>] -Endpoint <Uri>
 [-AuthenticationMode <NotificationSubscriberAuthMode>] [-AuthenticationUsername <String>]
 [-AuthenticationPassword <String>] [-Force] [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ConnectionParameters
```
Set-MgmtSvcNotificationSubscriber [-NotificationSubscriber <NotificationSubscriber>] -Name <String>
 [-Enabled <Boolean>] [-SubscriberType <NotificationSubscriberType>] -Endpoint <Uri>
 [-AuthenticationMode <NotificationSubscriberAuthMode>] [-AuthenticationUsername <String>]
 [-AuthenticationPassword <String>] [-Force] [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-Database <String>] [-Server <String>] [-UserName <String>] [-Password <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ConnectionString
```
Set-MgmtSvcNotificationSubscriber [-NotificationSubscriber <NotificationSubscriber>] -Name <String>
 [-Enabled <Boolean>] [-SubscriberType <NotificationSubscriberType>] -Endpoint <Uri>
 [-AuthenticationMode <NotificationSubscriberAuthMode>] [-AuthenticationUsername <String>]
 [-AuthenticationPassword <String>] [-Force] [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-ConnectionString <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject
```
Set-MgmtSvcNotificationSubscriber [-NotificationSubscriber <NotificationSubscriber>] [-Force]
 [-EncryptionKey <String>] [-EncryptionAlgorithm <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcNotificationSubscriber** cmdlet adds or updates a notification subscriber.
If the subscriber does not exist, the cmdlet adds a subscriber.
To update an existing notification subscriber, use the *Force* parameter.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

This cmdlet also assumes that the usage service is installed on the local computer.
If the usage service is installed on another computer, you must use the *EncryptionKey* and *EncryptionAlgorithm* parameters.

## EXAMPLES

### Example 1: Add a notification subscriber
```
PS C:\>Set-MgmtSvcNotificationSubscriber -AuthenticationMode None -Enabled $False -Endpoint https://localhost/ -Name "Billing" -SubscriberType BillingService
```

This command adds a notification subscriber to the database.
The command specifies a name and subscriber type for the notification subscriber.

### Example 2: Modify a notification subscriber
```
PS C:\>$Subscriber = Get-MgmtSvcNotificationSubscriber -Name "Billing"PS C:\> $Subscriber.AuthenticationMode = 'Basic'PS C:\> $Subscriber.AuthenticationUsername = 'MyUser'PS C:\> $Subscriber.AuthenticationPassword = 'PassWord'PS C:\> Set-MgmtSvcNotificationSubscriber -NotificationSubscriber $Subscriber -Force
```

The first command gets the notification subscriber named Billing and stores the object in the $Subscriber variable.

The second, third, and fourth commands make changes to the object stored in the $Subscriber variable.

The last command saves the modified notification subscriber object.
Using the *Force* parameter indicates that the existing subscriber is updated.

## PARAMETERS

### -AuthenticationMode
Specifies the authentication mode.
Valid values for this parameter are: 

- None
- Basic
- Windows

```yaml
Type: NotificationSubscriberAuthMode
Parameter Sets: ByProperties, ConnectionParameters, ConnectionString
Aliases: 
Accepted values: None, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationPassword
Specifies a password.

```yaml
Type: String
Parameter Sets: ByProperties, ConnectionParameters, ConnectionString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationUsername
Specifies a user name.

```yaml
Type: String
Parameter Sets: ByProperties, ConnectionParameters, ConnectionString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Enabled
Indicates whether the notification subscriber is enabled.

```yaml
Type: Boolean
Parameter Sets: ByProperties, ConnectionParameters, ConnectionString
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

### -Endpoint
Specifies a URI for the notification subscriber.

```yaml
Type: Uri
Parameter Sets: ByProperties, ConnectionParameters, ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Indicates that the cmdlet updates an existing subscriber.

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
Specifies the name of a notification subscriber.

```yaml
Type: String
Parameter Sets: ByProperties, ConnectionParameters, ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationSubscriber
Specifies a notification subscriber object.
To obtain a notification subscriber object, use the **Get-MgmtSvcNotificationSubscriber** cmdlet.
If you specify a notification subscriber object, the cmdlet changes that object, regardless of the *Name* parameter.

```yaml
Type: NotificationSubscriber
Parameter Sets: ConnectionParameters, ConnectionString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: NotificationSubscriber
Parameter Sets: ByObject
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

### -SubscriberType
Specifies a notification subscriber type.
Valid values for this parameter are: 

- BillingService
- MandatoryService
- OptionalService

```yaml
Type: NotificationSubscriberType
Parameter Sets: ByProperties, ConnectionParameters, ConnectionString
Aliases: 
Accepted values: BillingService, MandatoryService, OptionalService

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

[Remove-MgmtSvcNotificationSubscriber](xref:Configuration/v1.0/Remove-MgmtSvcNotificationSubscriber.md)


