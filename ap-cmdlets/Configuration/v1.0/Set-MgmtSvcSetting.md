---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 8BB9874F-DDDE-4ED9-B4B1-B8872C1C3B82
online version: http://go.microsoft.com/fwlink/?LinkID=296555
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcSetting.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcSetting.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcSetting.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcSetting

## SYNOPSIS
Changes settings of a management service component in the local web.config file.

## SYNTAX

```
Set-MgmtSvcSetting [-Namespace] <String> [-Name] <String> [[-Value] <String>] [-Encode] [-SkipUpdateHash]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcSetting** cmdlet changes configuration settings for a management service component.
You can use this cmdlet to change the values for the specified settings in the specified namespace.
You can also make updates to machine keys and credentials, and enable server certificate validation.

You must run this cmdlet on the computer that hosts the management services.

## EXAMPLES

### Example 1: Enable server certificate validation
```
PS C:\> Set-MgmtSvcSetting -Namespace "AdminSite" -Name DisableCertificateValidation" -Value False
```

This command enables server certificate validation for the AdminSite namespace.

## PARAMETERS

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

### -Encode
Indicates that the management service encodes the setting.

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

### -Name
Specifies the name of the management service setting.

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

### -Namespace
Specifies an array of namespaces of management service settings.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipUpdateHash
Indicates that the cmdlet does not update the hash table when it modifies a setting.

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

### -Value
Specifies the value of a setting.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

[Get-MgmtSvcSetting](xref:Configuration/v1.0/Get-MgmtSvcSetting.md)

[Protect-MgmtSvcConfiguration](xref:Configuration/v1.0/Protect-MgmtSvcConfiguration.md)

[Unprotect-MgmtSvcConfiguration](xref:Configuration/v1.0/Unprotect-MgmtSvcConfiguration.md)


