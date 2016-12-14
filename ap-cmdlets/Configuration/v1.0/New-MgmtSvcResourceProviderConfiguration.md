---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 52663C4C-C7A3-4226-9D93-ADEA0E767C27
online version: http://go.microsoft.com/fwlink/?LinkID=296549
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcResourceProviderConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcResourceProviderConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcResourceProviderConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-MgmtSvcResourceProviderConfiguration

## SYNOPSIS
Creates a resource provider.

## SYNTAX

```
New-MgmtSvcResourceProviderConfiguration [[-Name] <String>] [[-InstanceId] <String>] [-DisplayName <String>]
 [-InstanceDisplayName <String>] [-Type <ResourceProviderType>] [-AllowAnonymousAccess]
 [-AllowMultipleInstances] [-AdminForwardingAddress <String>] [-AdminAuthenticationMode <AuthenticationMode>]
 [-AdminAuthenticationUserName <String>] [-AdminAuthenticationPassword <String>]
 [-TenantForwardingAddress <String>] [-TenantAuthenticationMode <AuthenticationMode>]
 [-TenantAuthenticationUserName <String>] [-TenantAuthenticationPassword <String>]
 [-TenantSourceUriTemplate <String>] [-TenantTargetUriTemplate <String>] [-UsageForwardingAddress <String>]
 [-UsageAuthenticationMode <AuthenticationMode>] [-UsageAuthenticationUserName <String>]
 [-UsageAuthenticationPassword <String>] [-NotificationForwardingAddress <String>]
 [-NotificationAuthenticationMode <AuthenticationMode>] [-NotificationAuthenticationUserName <String>]
 [-NotificationAuthenticationPassword <String>] [-Input <String>] [-From <String>]
 [-ResourceProvider <ResourceProvider>] [-As <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-MgmtSvcResourceProviderConfiguration** cmdlet creates a resource provider in memory.
To add the resource provider, use the **Add-MgmtSvcResourceProviderConfiguration** cmdlet.

## EXAMPLES

### Example 1: Create a resource provider
```
PS C:\>$ConnectionString = ""
PS C:\> $EncryptionKey = "D576FCB3740049D44183C8BD6AB7979FB68DF253A1AFAB1BEDD987907358397D"
PS C:\> $EncryptionAlgorithm = "AES"
PS C:\> $UserName = "PattiFuller"
PS C:\> $Password = "passw0rd"
PS C:\> $RP = New-MgmtSvcResourceProviderConfiguration -Name 'RP01' `
-DisplayName 'Resource Provider 01' `
-AdminForwardingAddress "https://$Env:ComputerName`:30010/" `
-AdminAuthenticationMode 'Basic' `
-AdminAuthenticationUserName $UserName `
-AdminAuthenticationPassword $Password `
-TenantForwardingAddress "https://$Env:ComputerName`:30010/subscriptions" `
-TenantAuthenticationMode 'Basic' `
-TenantAuthenticationUserName $UserName `
-TenantAuthenticationPassword $Password `
-TenantSourceUriTemplate '{subid}/services/sqlservers/{*path}' `
-TenantTargetUriTemplate '{subid}/{*path}' `
-UsageForwardingAddress "https://$Env:ComputerName`:30010/" `
-UsageAuthenticationMode 'Basic' `
-UsageAuthenticationUserName $UserName `
-UsageAuthenticationPassword $Password `
-NotificationForwardingAddress "https://$Env:ComputerName`:30010/" `
-NotificationAuthenticationMode 'Basic' `
-NotificationAuthenticationUserName $UserName `
-NotificationAuthenticationPassword $Password
PS C:\> $RP
```

The first command stores a connection string in the $ConnectionString variable.

The second command stores an encryption key in the $EncryptionKey variable.

The third command specifies the encryption algorithm AES and stores the value in the $EncryptionAlgorighm variable.

The fourth command stores a user name in the $UserName variable.

The fifth command stores a password in the $Password variable.

The sixth command uses the provided information to create a resource provider for SQL servers, and stores the resource provider object in the $RP variable.

The last command displays information about the new resource provider to the user.
You can also use this variable to pass the resource provider object to other cmdlets, such as **Add-MgmtSvcResourceProviderConfiguration**.

## PARAMETERS

### -AdminAuthenticationMode
Specifies the administrative authentication mode of a resource provider.
Valid values for this parameter are:

- None
- Basic
- Windows

```yaml
Type: AuthenticationMode
Parameter Sets: (All)
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdminAuthenticationPassword
Specifies an administrator password to connect to a resource provider.

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

### -AdminAuthenticationUserName
Specifies an administrator user name to connect to a resource provider.

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

### -AdminForwardingAddress
Specifies an administrator forwarding address for a resource provider.

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

### -AllowAnonymousAccess
Indicates that anonymous access is allowed to a resource provider.

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

### -AllowMultipleInstances
Indicates that the cmdlet allows multiple instances of a resource provider.

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

### -As
Specifies an output format.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xml, XDocument, XmlString

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
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -From
Specifies the sender address.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Registry

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Input
Specifies input to a resource provider.

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

### -InstanceDisplayName
Specifies a display name for an instance of a resource provider.

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

### -InstanceId
Specifies an ID for an instance of a resource provider.

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

### -Name
Specifies the name of a resource provider

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

### -NotificationAuthenticationMode
Specifies the notification authentication mode for a resource provider.
Valid values for this parameter are:

- None
- Basic
- Windows

```yaml
Type: AuthenticationMode
Parameter Sets: (All)
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationAuthenticationPassword
Specifies a notification password to connect to a resource provider.

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

### -NotificationAuthenticationUserName
Specifies a notification user name to connect to a resource provider.

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

### -NotificationForwardingAddress
Specifies the notification forwarding address of a resource provider.

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

### -ResourceProvider
Specifies a resource provider.

```yaml
Type: ResourceProvider
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Parameter Sets: (All)
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantAuthenticationPassword
Specifies the tenant password to connect to a resource provider.

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

### -TenantAuthenticationUserName
Specifies the tenant user name to connect to a resource provider.

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

### -TenantForwardingAddress
Specifies the tenant forwarding address of a resource provider.

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

### -TenantSourceUriTemplate
Specifies the tenant source URI template of a resource provider.

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

### -TenantTargetUriTemplate
Specifies the tenant target URI template of a resource provider.

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

### -Type
Specifies the type of the resource provider.

```yaml
Type: ResourceProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, UsageProvider, CloudServiceProvider

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Parameter Sets: (All)
Aliases: 
Accepted values: None, Basic, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsageAuthenticationPassword
Specifies the usage password to connect to a resource provider.

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

### -UsageAuthenticationUserName
Specifies the usage user name to connect to a resource provider.

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

### -UsageForwardingAddress
Specifies the notification forwarding address of a resource provider.

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

[Add-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Add-MgmtSvcResourceProviderConfiguration.md)

[Get-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Get-MgmtSvcResourceProviderConfiguration.md)

[Remove-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Remove-MgmtSvcResourceProviderConfiguration.md)


