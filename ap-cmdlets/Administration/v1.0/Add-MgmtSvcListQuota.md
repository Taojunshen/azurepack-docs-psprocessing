---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 02AAFCBA-EE4A-459E-8644-4705ADFFB295
online version: http://go.microsoft.com/fwlink/?LinkID=316323
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcListQuota.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcListQuota.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Add-MgmtSvcListQuota.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcListQuota

## SYNOPSIS
Adds a list quota.

## SYNTAX

### ByProperties (Default)
```
Add-MgmtSvcListQuota [-QuotaList] <PlanQuotaUpdate> [-ServiceName] <String> [-ServiceInstanceId] <String>
 [<CommonParameters>]
```

### ByObject
```
Add-MgmtSvcListQuota [-QuotaList] <PlanQuotaUpdate> [[-Quota] <ServiceQuota>] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcListQuota** cmdlet adds a list quota.

## EXAMPLES

### Example 1: Add a list quota
```
PS C:\>$sqlserverRP = Get-MgmtSvcResourceProvider -AdminUri "https://Computer01:30004" -Token $Token -DisableCertificateValidation -Name sqlservers
PS C:\> $QuotaList = New-MgmtSvcQuotaList
PS C:\> Add-MgmtSvcListQuota -QuotaList $QuotaList -ServiceName sqlservers -ServiceInstanceId $sqlserverRP.InstanceId
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

The first command gets the resource provider object named sqlservers and stores the object in ther $sqlserverRP variable.

The second command creates a quota list and stores the quota list object in the $QuotaList variable.

The last command adds the list quota.

## PARAMETERS

### -Quota
Specifies a service quota object.

```yaml
Type: ServiceQuota
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -QuotaList
Specifies a quota list object.
To create a quota list object, use the **New-MgmtSvcQuotaList** cmdlet.

```yaml
Type: PlanQuotaUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceInstanceId
Specifies the ID of a service instance.

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

### -ServiceName
Specifies the name of a service.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-MgmtSvcQuotaList](xref:Administration/v1.0/New-MgmtSvcQuotaList.md)


