---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 214BC170-8249-41AC-9CE1-7CD43D24C87E
online version: http://go.microsoft.com/fwlink/?LinkID=316322
schema: 2.0.0
updated_at: 1/4/2017 5:31 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcPlan.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcPlan.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/93767eba34ad89edb3696359a7595e41769e0346/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcPlan.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcPlan

## SYNOPSIS
Adds a service plan to Windows Azure Pack.

## SYNTAX

### ByProperties (Default)
```
Add-MgmtSvcPlan [-DisplayName] <String> [[-State] <PlanState>] [[-MaxSubscriptionsPerAccount] <Int32>]
 [[-InvitationCode] <String>] [[-Price] <String>] [[-SecurityGroup] <String[]>] [-AdminUri] <Uri>
 [-Token] <String> [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject
```
Add-MgmtSvcPlan [[-Plan] <Plan>] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcPlan** adds a service plan to Windows Azure Pack for Windows Server.
A service plan defines the resources, capabilities, and limitations of the hosting services that are offered to a tenant according to a scope that is determined by the hosting service provider.

## EXAMPLES

### Example 1: Add a service plan
```
PS C:\> Add-MgmtSvcPlan -AdminURI "https://Computer01:30004" -Token $Token -DisplayName "Service Plan 01" -State Public -MaxSubscriptionsPerAccount 15 -InvitationCode "Welcome01" -Price "300"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command creates a service plan named Service Plan 01.

## PARAMETERS

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

### -DisplayName
Specifies the display name of the plan.

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

### -InvitationCode
Specifies the invitation code for the plan.
This code allows tenants to subscribe to the plan.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxSubscriptionsPerAccount
Specifies the maximum subscriptions that are allowed per account for the plan.

```yaml
Type: Int32
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plan
Specifies a plan object.
To get a plan object, use the **Get-MgmtSvcPlan** cmdlet.

```yaml
Type: Plan
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Price
Specifies the price for subscribing to the plan.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecurityGroup
Specifies an array of security groups that can be associated with a plan.
The plan is only visible for subscription by members of these security groups.

```yaml
Type: String[]
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Specifies the state of the plan.
Valid values are:

- Public. Tenants can subscribe to a plan only when it is public.
- Private. This is the initial state of a plan after it is created.
- Decomissioned. The plan is active, but will not accept any new subscriptions.

```yaml
Type: PlanState
Parameter Sets: ByProperties
Aliases: 
Accepted values: Private, Public, Decommissioned

Required: False
Position: 3
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

[Get-MgmtSvcPlan](xref:Administration/v1.0/Get-MgmtSvcPlan.md)

[Set-MgmtSvcPlan](xref:Administration/v1.0/Set-MgmtSvcPlan.md)

[Sync-MgmtSvcPlan](xref:Administration/v1.0/Sync-MgmtSvcPlan.md)

[Remove-MgmtSvcPlan](xref:Administration/v1.0/Remove-MgmtSvcPlan.md)


