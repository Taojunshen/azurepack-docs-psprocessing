---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 859E15B4-0656-4B7A-88D4-EC8AEF5BD9C0
online version: http://go.microsoft.com/fwlink/?LinkID=316361
schema: 2.0.0
updated_at: 1/4/2017 5:31 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Update-MgmtSvcAddOnQuota.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Update-MgmtSvcAddOnQuota.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/93767eba34ad89edb3696359a7595e41769e0346/AzurePack-cmdlets/Administration/v1.0/Update-MgmtSvcAddOnQuota.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Update-MgmtSvcAddOnQuota

## SYNOPSIS
Adds a quota list to an add-on.

## SYNTAX

```
Update-MgmtSvcAddOnQuota [-AddOnId] <String> [-QuotaList] <PlanQuotaUpdate> [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Update-MgmtSvcAddOnQuota** cmdlet adds a quota list to an add-on.

## EXAMPLES

### Example 1: Add a quota list to an add-on
```
PS C:\> New-MgmtSvcQuotaList | Update-MgmtSvcAddOnQuota -AdminUri "https://Computer01:30004" -Token $Token -AddOnId "7b337b38"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command creates a quota list and uses the pipeline operator to pass the quota list object to **Update-MgmtSvcAddOnQuota** which adds the quota list to the add-on with the ID of 7b337b38.

## PARAMETERS

### -AddOnId
Specifies the ID of an add-on.

```yaml
Type: String
Parameter Sets: (All)
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

### -QuotaList
Specifies a plan quota update object.
To create a quota list, use the **New-MgmtSvcQuotaList** cmdlet.

```yaml
Type: PlanQuotaUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
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

[New-MgmtSvcQuotaList](xref:Administration/v1.0/New-MgmtSvcQuotaList.md)

[Add-MgmtSvcListQuota](xref:Administration/v1.0/Add-MgmtSvcListQuota.md)

[Update-MgmtSvcPlanQuota](xref:Administration/v1.0/Update-MgmtSvcPlanQuota.md)


