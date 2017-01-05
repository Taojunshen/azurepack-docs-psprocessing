---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 5B95E537-4759-4D6F-9A1D-711777A4F593
online version: http://go.microsoft.com/fwlink/?LinkID=316347
schema: 2.0.0
updated_at: 1/4/2017 5:31 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Remove-MgmtSvcPlan.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Remove-MgmtSvcPlan.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/93767eba34ad89edb3696359a7595e41769e0346/AzurePack-cmdlets/Administration/v1.0/Remove-MgmtSvcPlan.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-MgmtSvcPlan

## SYNOPSIS
Removes a service plan from Windows Azure Pack.

## SYNTAX

```
Remove-MgmtSvcPlan [-PlanId] <String> [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MgmtSvcPlan** removes a service plan from Windows Azure Pack for Windows Server.

## EXAMPLES

### Example 1: Remove a service plan
```
PS C:\> Remove-MgmtSvcPlan -AdminUri "https://Computer01:30004" -Token $Token -PlanId "4396660b" -Confirm
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command removes the service plan with the ID of 4396660b, and prompts the user for confirmation before removing the plan.

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

### -PlanId
Specifies the ID of a plan.

```yaml
Type: String
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

[Add-MgmtSvcPlan](xref:Administration/v1.0/Add-MgmtSvcPlan.md)

[Get-MgmtSvcPlan](xref:Administration/v1.0/Get-MgmtSvcPlan.md)

[Set-MgmtSvcPlan](xref:Administration/v1.0/Set-MgmtSvcPlan.md)

[Sync-MgmtSvcPlan](xref:Administration/v1.0/Sync-MgmtSvcPlan.md)


