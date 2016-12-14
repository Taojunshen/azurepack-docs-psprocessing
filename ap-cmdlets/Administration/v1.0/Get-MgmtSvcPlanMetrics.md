---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 71062D03-FBB4-416D-B32B-C125B881993F
online version: http://go.microsoft.com/fwlink/?LinkID=316336
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcPlanMetrics.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcPlanMetrics.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcPlanMetrics.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcPlanMetrics

## SYNOPSIS
Gets the metrics for a service plan.

## SYNTAX

```
Get-MgmtSvcPlanMetrics [-PlanId] <String> [[-StartTime] <DateTime>] [[-EndTime] <DateTime>] [-AdminUri] <Uri>
 [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcPlanMetrics** cmdlet gets the metrics for a service plan.

## EXAMPLES

### Example 1: Get metrics for a service plan
```
PS C:\>Get-MgmtSvcPlanMetrics -PlanId 'Examphmdwwdi2' -AdminUri "https://Computer01:30004" -Token $Token -DisableCertificateValidation
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets metrics for the plan with the ID Examphmdwwdi2.

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

### -EndTime
Specifies the end of the date range as a DateTime object.
To obtain a DateTime object, use the **Get-Date** cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -StartTime
Specifies the start of the date range as a DateTime object.
To obtain a DateTime object, use the **Get-Date** cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MgmtSvcPlan](xref:Administration/v1.0/Get-MgmtSvcPlan.md)


