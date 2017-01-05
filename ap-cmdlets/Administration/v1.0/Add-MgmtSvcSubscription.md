---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: E163BD15-FE0F-45F4-9C75-4636FD556203
online version: http://go.microsoft.com/fwlink/?LinkID=316328
schema: 2.0.0
updated_at: 1/4/2017 5:31 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcSubscription.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcSubscription.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/93767eba34ad89edb3696359a7595e41769e0346/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcSubscription.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcSubscription

## SYNOPSIS
Adds a subscription.

## SYNTAX

### ByProperties (Default)
```
Add-MgmtSvcSubscription [-AccountAdminLiveEmailId] <String> [-AccountAdminLivePuid] <String>
 [-FriendlyName] <String> [-PlanId] <String> [[-SubscriptionId] <Guid>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject
```
Add-MgmtSvcSubscription [[-ProvisioningInfo] <AzureProvisioningInfo>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcSubscription** cmdlet adds a subscription.

## EXAMPLES

### Example 1: Add a subscription
```
PS C:\> Add-MgmtSvcSubscription -AdminUri "https://Computer01:30004" -Token $Token -AccountAdminLiveEmailId 'user@Contoso.com' -AccountAdminLivePuid 'user@Contoso.com' -PlanId 'e3a1c7e1' -FriendlyName 'MySubcription01' -DisableCertificateValidation
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command adds a subscription named MySubscription01.

## PARAMETERS

### -AccountAdminLiveEmailId
Specifies the email ID for the account administrator.

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

### -AccountAdminLivePuid
Specifies the passport unique identifier (PUID) for the account administrator.

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

### -FriendlyName
Specifies a friendly name for the subscription.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanId
Specifies the ID of a plan.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisioningInfo
Specifies a Windows Azure provisioning information object.

```yaml
Type: AzureProvisioningInfo
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SubscriptionId
Specifies an ID for a subscription.

```yaml
Type: Guid
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Token
Specifies an identity token.
To create a token, use the [Get-MgmtSvcToken](./Get-MgmtSvcToken.md) cmdlet.

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

[Get-MgmtSvcToken](xref:Administration/v1.0/Get-MgmtSvcToken.md)

[Get-MgmtSvcSubscription](xref:Administration/v1.0/Get-MgmtSvcSubscription.md)

[Disable-MgmtSvcSubscription](xref:Administration/v1.0/Disable-MgmtSvcSubscription.md)

[Enable-MgmtSvcSubscription](xref:Administration/v1.0/Enable-MgmtSvcSubscription.md)

[Move-MgmtSvcSubscription](xref:Administration/v1.0/Move-MgmtSvcSubscription.md)

[Remove-MgmtSvcSubscription](xref:Administration/v1.0/Remove-MgmtSvcSubscription.md)


