---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 70015B7E-6F2C-4DFA-B3C7-B7099EEE7372
online version: http://go.microsoft.com/fwlink/?LinkID=316324
schema: 2.0.0
updated_at: 1/4/2017 6:48 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcResourceProvider.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcResourceProvider.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/97a55db972036fa7bf413cbe2fbdbe06fef1d3a1/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcResourceProvider.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcResourceProvider

## SYNOPSIS
Adds a resource provider to a management store database.

## SYNTAX

### ByProperties (Default)
```
Add-MgmtSvcResourceProvider [-Name] <String> [-DisplayName] <String> [[-Description] <String>]
 [[-Enabled] <Boolean>] [[-PassThroughEnabled] <Boolean>] [[-AllowAnonymousAccess] <Boolean>]
 [[-AllowMultipleInstances] <Boolean>] [[-AdminForwardingAddress] <Uri>]
 [[-AdminAuthenticationMode] <AuthenticationMode>] [[-AdminAuthenticationUser] <PSCredential>]
 [[-TenantForwardingAddress] <Uri>] [[-TenantAuthenticationMode] <AuthenticationMode>]
 [[-TenantAuthenticationUsername] <String>] [[-TenantAuthenticationPassword] <String>]
 [[-UsageForwardingAddress] <Uri>] [[-UsageAuthenticationMode] <AuthenticationMode>]
 [[-UsageAuthenticationUsername] <String>] [[-UsageAuthenticationPassword] <String>]
 [[-HealthCheckForwardingAddress] <Uri>] [[-HealthCheckAuthenticationMode] <AuthenticationMode>]
 [[-HealthCheckAuthenticationUsername] <String>] [[-HealthCheckAuthenticationPassword] <String>]
 [[-NotificationForwardingAddress] <Uri>] [[-NotificationAuthenticationMode] <AuthenticationMode>]
 [[-NotificationAuthenticationUsername] <String>] [[-NotificationAuthenticationPassword] <String>]
 [[-InstanceId] <Guid>] [-InstanceDisplayName] <String> [[-MaxQuotaUpdateBatchSize] <Int32>]
 [[-SubscriptionStatusPollingInterval] <TimeSpan>] [[-Type] <ResourceProviderType>] [-AdminUri] <Uri>
 [-Token] <String> [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject
```
Add-MgmtSvcResourceProvider [[-ResourceProvider] <ResourceProvider>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcResourceProvider** cmdlet adds a resource provider entry in a management store database.
You can run this cmdlet from any computer in the deployment.

## EXAMPLES

### Example 1: Add a resource provider
```
PS C:\> $UserName = "PattiFuller"
PS C:\> $Password = "passw0rd"
PS C:\> $AdminUser = Get-Credential
PS C:\> Add-MgmtSvcResourceProvider -AdminURI "https://Computer01:30004" -Token $Token -Name "ResourceProvider02" -DisplayName "Resource Provider 02" -AllowMultipleInstances $True -AdminForwardingAddress "https://$env:ComputerName`:30010/" -AdminAuthenticationMode "Basic" -AdminAuthenticationUser $AdminUser -TenantForwardingAddress "https://$Env:ComputerName`:30010/subscriptions" -TenantAuthenticationMode "Basic" -TenantAuthenticationUserName $UserName -TenantAuthenticationPassword $Password -UsageForwardingAddress "https://$Env:ComputerName`:30010/" -UsageAuthenticationMode "Basic" -UsageAuthenticationUserName $UserName -UsageAuthenticationPassword -Password -HealthCheckForwardingAddress "https://$Env:ComputerName`:30010/" -HealthCheckAuthenticationMode "Basic" -HealthCheckAuthenticationUserName $UserName -HealthCheckAuthenticationPassword $Password -NotificationForwardingAddress "https://$Env:ComputerName`:30010/" -NotificationAuthenticationMode "Basic" -NotificationAuthenticationUsername $UserName -NotificationAuthenticationPassword $Password -InstanceDisplayName "Resource Provider 02.1" -Type "Standard"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

The first command stores a user name in the $UserName variable.

The second command stores a password in the $Password variable.

The third command prompts the user for credentials and stores the resulting **PSCredential** object in the $AdminUser variable.

The last command adds a resource provider.

## PARAMETERS

### -AdminAuthenticationMode
Specifies the administrative authentication mode of a resource provider.
Valid values for this parameter are:

- None
- Basic
- Windows

```yaml
Type: AuthenticationMode
Parameter Sets: ByProperties
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminAuthenticationUser
Specifies, as a **PSCredential** object, an administrative user name and password to connect to a resource provider.
To get a **PSCredential** object, use the **Get-Credential** cmdlet.

```yaml
Type: PSCredential
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminForwardingAddress
Specifies an administrator forwarding address for a resource provider.

```yaml
Type: Uri
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUri
Specifies the URI of the Windows Azure Pack administrator API.
Use the following format: https://\<computer\>:\<port\>, where \<computer\> is the computer on which the administrator API is installed.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AllowAnonymousAccess
Indicates that anonymous access is allowed to a resource provider.

```yaml
Type: Boolean
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AllowMultipleInstances
Indicates that the cmdlet allows multiple instances of the resource provider.

```yaml
Type: Boolean
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Description
Specifies a description for the resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableCertificateValidation
Disables certificate validation for the Windows Azure Pack installation.

If you specify this parameter, you can use self-signed certificates.

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

### -DisplayName
Specifies the display name of a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Enabled
Enables the resource provider.

```yaml
Type: Boolean
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HealthCheckAuthenticationMode
Specifies the health check authentication mode for a resource provider.
Valid values for this parameter are:

- None
- Basic
- Windows

```yaml
Type: AuthenticationMode
Parameter Sets: ByProperties
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HealthCheckAuthenticationPassword
Specifies a health check password to connect to a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 24
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HealthCheckAuthenticationUsername
Specifies a health check user name to connect to a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 23
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HealthCheckForwardingAddress
Specifies the health check forwarding address for a resource provider.

```yaml
Type: Uri
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceDisplayName
Specifies a display name for an instance of a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 30
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceId
Specifies an ID for an instance of a resource provider.

```yaml
Type: Guid
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 29
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxQuotaUpdateBatchSize
Specifies the number of subscriptions that can be updated in a single request.
The default value is 5.

```yaml
Type: Int32
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 31
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name of a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationAuthenticationMode
Specifies the notification authentication mode for a resource provider.
Valid values for this parameter are:

- None
- Basic
- Windows

```yaml
Type: AuthenticationMode
Parameter Sets: ByProperties
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: 26
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationAuthenticationPassword
Specifies a notification password to connect to a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 28
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationAuthenticationUsername
Specifies a notification user name to connect to a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 27
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationForwardingAddress
Specifies the notification forwarding address of a resource provider.

```yaml
Type: Uri
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 25
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThroughEnabled
Indicates whether the resource provider supports API pass-through.

```yaml
Type: Boolean
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Specifies a resource provider object.

```yaml
Type: ResourceProvider
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SubscriptionStatusPollingInterval
Specifies the time interval at which the management service polls the resource provider for subscription status updates.
The default is 10 seconds.

Format this value in the standard JASON serialized timespan of 00:00:00.
For example, 10 seconds is formatted as 00:00:10.

```yaml
Type: TimeSpan
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 32
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantAuthenticationMode
Specifies the tenant authentication mode of a resource provider.
Valid values for this parameter are:

- None
- Basic
- Windows

```yaml
Type: AuthenticationMode
Parameter Sets: ByProperties
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantAuthenticationPassword
Specifies the tenant password to connect to a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantAuthenticationUsername
Specifies the tenant user name to connect to a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantForwardingAddress
Specifies the tenant forwarding address of a resource provider.

```yaml
Type: Uri
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Token
Specifies an identity token.
To create a token, use the **Get-MgmtSvcToken** cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
Specifies the type of the resource provider.
Valid values for this parameter are:

- Standard
- UsageProvider
- CloudServiceProvider

```yaml
Type: ResourceProviderType
Parameter Sets: ByProperties
Aliases: 
Accepted values: Standard, UsageProvider, CloudServiceProvider

Required: False
Position: 33
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UsageAuthenticationMode
Specifies the usage authentication mode of a resource provider.
Valid values for this parameter are:

- None
- Basic
- Windows

```yaml
Type: AuthenticationMode
Parameter Sets: ByProperties
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UsageAuthenticationPassword
Specifies the usage password to connect to a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UsageAuthenticationUsername
Specifies the usage user name to connect to a resource provider.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UsageForwardingAddress
Specifies the notification forwarding address of a resource provider.

```yaml
Type: Uri
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Get-MgmtSvcResourceProvider](xref:Administration/v1.0/Get-MgmtSvcResourceProvider.md)

[Set-MgmtSvcResourceProvider](xref:Administration/v1.0/Set-MgmtSvcResourceProvider.md)

[Test-MgmtSvcResourceProvider](xref:Administration/v1.0/Test-MgmtSvcResourceProvider.md)

[Remove-MgmtSvcResourceProvider](xref:Administration/v1.0/Remove-MgmtSvcResourceProvider.md)


