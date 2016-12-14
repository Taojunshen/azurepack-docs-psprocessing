---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 788D923D-B540-4D78-A2A1-9ED10FF3F914
online version: http://go.microsoft.com/fwlink/?LinkID=316327
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcQuotaSetting.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcQuotaSetting.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcQuotaSetting.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcQuotaSetting

## SYNOPSIS
Adds a setting to a quota.

## SYNTAX

### ByProperties (Default)
```
Add-MgmtSvcQuotaSetting [-Quota] <ServiceQuota> [-Key] <String> [-Value] <String> [<CommonParameters>]
```

### ByObject
```
Add-MgmtSvcQuotaSetting [-Quota] <ServiceQuota> [[-Setting] <ServiceQuotaSetting>] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcQuotaSetting** cmdlet adds a setting to a quota object.

## EXAMPLES

### Example 1: Add a quota setting
```
PS C:\>$sqlserverRP = Get-MgmtSvcResourceProvider -AdminUri "https://Computer01:30004" -Token $Token -DisableCertificateValidation -Name sqlservers
PS C:\> $QuotaList = New-MgmtSvcQuotaList
PS C:\> $SqlQuota = Add-MgmtSvcListQuota -QuotaList $QuotaList -ServiceName sqlservers -ServiceInstanceId $sqlserverRP.InstanceId 
PS C:\> Add-MgmtSvcQuotaSetting -Quota $SqlQouta -Key Editions -Value '[{"displayName":"Default","groupName":"Default","resourceCount":"10","resourceSize":"1024","resourceSizeLimit":"1024","offerEditionId":"081313063701","groupType":null}]'
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

The first command gets the resource provider object named sqlservers and stores the object in ther $sqlserverRP variable.

The second command creates a quota list and stores the quota list object in the $QuotaList variable.

The third command adds the list quota and stores the quota object in the $SqlQuota variable.

The last command adds the quota setting.

## PARAMETERS

### -Key
Specifies a key.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Quota
Specifies a service quota object.

```yaml
Type: ServiceQuota
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Setting
Specifies a quota setting.

```yaml
Type: ServiceQuotaSetting
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Specifies a value for the setting.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-MgmtSvcListQuota](xref:Administration/v1.0/Add-MgmtSvcListQuota.md)


