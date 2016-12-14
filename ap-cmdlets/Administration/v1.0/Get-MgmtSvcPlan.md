---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: F7DC14C8-298B-4F4E-990B-EE210C8B7934
online version: http://go.microsoft.com/fwlink/?LinkID=316335
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcPlan.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcPlan.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcPlan.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcPlan

## SYNOPSIS
Gets a service plan.

## SYNTAX

### ByDisplayName (Default)
```
Get-MgmtSvcPlan [[-DisplayName] <String[]>] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [<CommonParameters>]
```

### ByPlanId
```
Get-MgmtSvcPlan [-PlanId <String>] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcPlan** cmdlets gets a service plan.
If you run this cmdlet without specifying a display name, all plans are returned.
To get a specific plan, specifiy a display name.

## EXAMPLES

### Example 1: Get all service plans
```
PS C:\>Get-MgmtSvcPlan -AdminUri "https://Computer01:30004" -Token $Token
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command returns all service plans.

### Example 2: Get a service plan by its name
```
PS C:\>Get-MgmtSvcPlan -AdminUri "https://Computer01:30004" -Token $Token -DisplayName "Service Plan 01"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command returns the plan named Service Plan 01.

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

### -DisplayName
Specifies the display name of a plan.

```yaml
Type: String[]
Parameter Sets: ByDisplayName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanId
Specifies the ID for a plan.

```yaml
Type: String
Parameter Sets: ByPlanId
Aliases: 

Required: False
Position: Named
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

[Add-MgmtSvcPlan](xref:Administration/v1.0/Add-MgmtSvcPlan.md)

[Set-MgmtSvcPlan](xref:Administration/v1.0/Set-MgmtSvcPlan.md)

[Sync-MgmtSvcPlan](xref:Administration/v1.0/Sync-MgmtSvcPlan.md)

[Remove-MgmtSvcPlan](xref:Administration/v1.0/Remove-MgmtSvcPlan.md)


