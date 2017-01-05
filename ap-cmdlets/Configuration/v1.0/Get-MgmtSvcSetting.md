---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: E564243B-DC16-4DCE-8E87-9B4CAC2EDA51
online version: http://go.microsoft.com/fwlink/?LinkID=296542
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcSetting.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcSetting.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcSetting.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcSetting

## SYNOPSIS
Gets the local setting values for the management service component.

## SYNTAX

```
Get-MgmtSvcSetting [[-Namespace] <String[]>] [[-Name] <String[]>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcSetting** cmdlet gets the local setting values for the management service component.
The cmdlet returns the namespace, name, and value of the management service component.

## EXAMPLES

### Example 1: Get the machine key setting
```
PS C:\> Get-MgmtSvcSetting -Namespace "TenantSite" -Name "machineKey.decryptionKey"
```

This command gets the machine key on the tenant site on the local computer.

## PARAMETERS

### -Name
Specifies an array of names of management service settings.
You can use wildcard characters.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Specifies an array of namespaces of management service settings.
You can use wildcards.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-MgmtSvcSetting](xref:Configuration/v1.0/Set-MgmtSvcSetting.md)

[Protect-MgmtSvcConfiguration](xref:Configuration/v1.0/Protect-MgmtSvcConfiguration.md)

[Unprotect-MgmtSvcConfiguration](xref:Configuration/v1.0/Unprotect-MgmtSvcConfiguration.md)

[Get-MgmtSvcDatabaseSetting](xref:Configuration/v1.0/Get-MgmtSvcDatabaseSetting.md)

[Set-MgmtSvcDatabaseSetting](xref:Configuration/v1.0/Set-MgmtSvcDatabaseSetting.md)


