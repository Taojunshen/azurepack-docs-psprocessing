---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 01D1B20B-B041-4A39-9E8C-B719EE6B33D5
online version: http://go.microsoft.com/fwlink/?LinkID=316357
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Sync-MgmtSvcAddOn.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Sync-MgmtSvcAddOn.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Sync-MgmtSvcAddOn.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Sync-MgmtSvcAddOn

## SYNOPSIS
Synchronizes a service add-on.

## SYNTAX

```
Sync-MgmtSvcAddOn [-AddOnId] <String> [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Sync-MgmtSvcAddOn** cmdlet synchronizs a service add-on.

## EXAMPLES

### Example 1: Synchronize an add-on
```
PS C:\>Sync-MgmtSvcAddOn -AdminUri "https://Computer01:30004" -Token $Token -AddOnId "7b337b38"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command synchronizes the add-on with the id of 7b337b38.

## PARAMETERS

### -AddOnId
Specifies an ID for an add-on.

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

[Get-MgmtSvcAddOn](xref:Administration/v1.0/Get-MgmtSvcAddOn.md)

[Set-MgmtSvcAddOn](xref:Administration/v1.0/Set-MgmtSvcAddOn.md)

[Sync-MgmtSvcAddOn](xref:Administration/v1.0/Sync-MgmtSvcAddOn.md)

[Remove-MgmtSvcAddOn](xref:Administration/v1.0/Remove-MgmtSvcAddOn.md)

[Add-MgmtSvcAddOnService](xref:Administration/v1.0/Add-MgmtSvcAddOnService.md)

[Remove-MgmtSvcAddOnService](xref:Administration/v1.0/Remove-MgmtSvcAddOnService.md)


