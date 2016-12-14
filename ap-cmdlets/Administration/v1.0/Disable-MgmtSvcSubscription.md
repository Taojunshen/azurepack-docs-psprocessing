---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 1C494847-93FC-4887-BB6B-7D5F8E6A834E
online version: http://go.microsoft.com/fwlink/?LinkID=316330
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Disable-MgmtSvcSubscription.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Disable-MgmtSvcSubscription.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Disable-MgmtSvcSubscription.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Disable-MgmtSvcSubscription

## SYNOPSIS
Disables a subscription.

## SYNTAX

```
Disable-MgmtSvcSubscription [-SubscriptionId] <Guid> [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-MgmtSvcSubscription** cmdlet disables a subscription.
To enable a subscription, use the **Enable-MgmtSvcSubscription** cmdlet.

## EXAMPLES

### Example 1: Disable a subscription
```
PS C:\>Disable-MgmtSvcSubscription -SubscriptionId 'd5876082-8524-441e-b0ce-e2b582806df3' -AdminUri "https://Computer01:30004" -Token $Token -DisableCertificateValidation
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command disables the subscription with the ID d5876082-8524-441e-b0ce-e2b582806df3.

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

If you specifiy this parameter, you can use self-signed certificates.

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
Specifies the ID, as a GUID, of a subscription.

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

[Enable-MgmtSvcSubscription](xref:Administration/v1.0/Enable-MgmtSvcSubscription.md)

[Add-MgmtSvcSubscription](xref:Administration/v1.0/Add-MgmtSvcSubscription.md)

[Get-MgmtSvcSubscription](xref:Administration/v1.0/Get-MgmtSvcSubscription.md)

[Move-MgmtSvcSubscription](xref:Administration/v1.0/Move-MgmtSvcSubscription.md)

[Sync-MgmtSvcSubscription](xref:Administration/v1.0/Sync-MgmtSvcSubscription.md)

[Remove-MgmtSvcSubscription](xref:Administration/v1.0/Remove-MgmtSvcSubscription.md)


