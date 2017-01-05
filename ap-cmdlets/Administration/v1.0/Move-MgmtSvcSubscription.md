---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 29A65AA0-0C13-4E1A-BC20-A7CE197F8164
online version: http://go.microsoft.com/fwlink/?LinkId=325019
schema: 2.0.0
updated_at: 1/4/2017 5:31 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Move-MgmtSvcSubscription.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Move-MgmtSvcSubscription.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/93767eba34ad89edb3696359a7595e41769e0346/AzurePack-cmdlets/Administration/v1.0/Move-MgmtSvcSubscription.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Move-MgmtSvcSubscription

## SYNOPSIS
Migrates a subscription to a different plan.

## SYNTAX

```
Move-MgmtSvcSubscription [-SubscriptionId] <Guid> [-TargetPlanId] <String> [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Move-MgmtSvcSubscription** cmdlet migrates a subscription to a different plan.

## EXAMPLES

### Example 1: Move a subscription
```
PS C:\> Move-MgmtSvcSubscription -SubscriptionId 'd5876082-8524-441e-b0ce-e2b582806df3' -TargetPlanId 'Migrahme7xxzb' -AdminUri "https://Computer01:30004" -Token $Token -DisableCertificateValidation
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command moves the subscription with the ID d5876082-8524-441e-b0ce-e2b582806df3 to the plan with the ID Migrahme7xxzb.

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

### -SubscriptionId
Specifies the ID of a subscription.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetPlanId
Specifies the ID of the plan to which the subscription is migrated.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
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

[Add-MgmtSvcSubscription](xref:Administration/v1.0/Add-MgmtSvcSubscription.md)

[Get-MgmtSvcSubscription](xref:Administration/v1.0/Get-MgmtSvcSubscription.md)

[Disable-MgmtSvcSubscription](xref:Administration/v1.0/Disable-MgmtSvcSubscription.md)

[Enable-MgmtSvcSubscription](xref:Administration/v1.0/Enable-MgmtSvcSubscription.md)

[Sync-MgmtSvcSubscription](xref:Administration/v1.0/Sync-MgmtSvcSubscription.md)

[Remove-MgmtSvcSubscription](xref:Administration/v1.0/Remove-MgmtSvcSubscription.md)


