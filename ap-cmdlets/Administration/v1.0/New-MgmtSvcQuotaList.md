---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 7D94D10E-FE90-4772-8BFE-3C05DFD9934F
online version: http://go.microsoft.com/fwlink/?LinkID=316343
schema: 2.0.0
updated_at: 1/4/2017 5:31 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/New-MgmtSvcQuotaList.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/New-MgmtSvcQuotaList.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/93767eba34ad89edb3696359a7595e41769e0346/AzurePack-cmdlets/Administration/v1.0/New-MgmtSvcQuotaList.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-MgmtSvcQuotaList

## SYNOPSIS
Creates a quota list.

## SYNTAX

```
New-MgmtSvcQuotaList [<CommonParameters>]
```

## DESCRIPTION
The **New-MgmtSvcQuotaList** cmdlet creates a quota list.

## EXAMPLES

### Example 1: Create a quota list and update a plan
```
PS C:\> New-MgmtSvcQuotaList | Update-MgmtSvcPlanQuota -AdminUri "https://Computer01:30004" -Token $Token -PlanId "4396660b"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command creates a quota list and uses the pipeline operator to pass the quota list object to **Update-MgmtSvcPlanQuota** which adds the quota list to the plan with the ID of 4396660b.

### Example 2: Create a quota list and update an add-on
```
PS C:\> New-MgmtSvcQuotaList | Update-MgmtSvcAddOnQuota -AdminUri "https://Computer01:30004" -Token $Token -AddOnId "7b337b38"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command creates a quota list and uses the pipeline operator to pass the quota list object to **Update-MgmtSvcAddOnQuota** which adds the quota list to the add-on with the ID of 7b337b38.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Update-MgmtSvcPlanQuota](xref:Administration/v1.0/Update-MgmtSvcPlanQuota.md)

[Update-MgmtSvcAddOnQuota](xref:Administration/v1.0/Update-MgmtSvcAddOnQuota.md)


