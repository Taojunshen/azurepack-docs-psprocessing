---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 2FB4BCF9-DF92-4EC8-A73C-3510F425735B
online version: http://go.microsoft.com/fwlink/?LinkID=296536
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcResourceProviderConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcResourceProviderConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcResourceProviderConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcResourceProviderConfiguration

## SYNOPSIS
Adds a resource provider to Windows Azure Pack.

## SYNTAX

```
Add-MgmtSvcResourceProviderConfiguration [-ResourceProvider] <ResourceProvider> [-ConnectionString <String>]
 [-EncryptionKey <String>] [-EncryptionAlgorithm <String>] [-Force] [-As <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcResourceProviderConfiguration** cmdlet adds a resource provider to Windows Azure Pack for Windows Server.
You can run this cmdlet from any computer in the deployment.
If you run this cmdlet on the computer on which the Admin API service is installed and the Web.config file contains values for *ConnectionString*, *EncryptionKey*, and *EncryptionAlgorithm*, then those values are used.

## EXAMPLES

### Example 1: Add a resource provider
```
PS C:\> $ConnectionString = ""
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
PS C:\> Add-MgmtSvcResourceProviderConfiguration -ResourceProvider $RP
```

The first five commands set variables to use when creating a new resource provider.

The sixth command creates a resource provider and stores the resulting resource provider object in the $RP variable.
For information about creating a resource provider, see the **New-MgmtSvcResourceProviderConfiguration** cmdlet.

The last command adds the resource provider stored in $RP.

## PARAMETERS

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

### -Force
Updates an existing resource provider when one is found with the same name and instance ID of the one provided with this cmdlet.
If there is no existing resource provider with the provided name and instance ID, then the resource provider is added, and this parameter is ignored.

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

### -ResourceProvider
Specifies a resource provider.

```yaml
Type: ResourceProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

[New-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/New-MgmtSvcResourceProviderConfiguration.md)

[Get-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Get-MgmtSvcResourceProviderConfiguration.md)

[Remove-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Remove-MgmtSvcResourceProviderConfiguration.md)


