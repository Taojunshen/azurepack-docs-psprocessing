---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: E53E6FC0-91B4-4016-BD5D-267CEFDB3B83
online version: http://go.microsoft.com/fwlink/?LinkID=321258
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesPolicy.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesPolicy.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesPolicy.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-WebSitesPolicy

## SYNOPSIS
Removes a website site policy.

## SYNTAX

```
Remove-WebSitesPolicy [-PlanName] <String> [-ComputeMode] <ComputeModeOptions> [-SiteMode] <String>
 [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-WebSitesPolicy** cmdlet removes a website site policy.

## EXAMPLES

### Example 1: Remove a policy
```
PS C:\> Remove-WebSitesPolicy -PlanName "Plan01" -ComputeMode "Shared" -SiteMode "Basic"
```

This command removes the policy named Plan01.

## PARAMETERS

### -ComputeMode
Specifies the type of hosting environment that the web site runs in.
Valid values are:

- Shared. The web site runs in a shared/multi-tenant hosting environment. 
- Dedicated. The web site runs in its own dedicated hosting environment.

For example:

`-ComputeMode "Dedicated"`

```yaml
Type: ComputeModeOptions
Parameter Sets: (All)
Aliases: 
Accepted values: Shared, Dedicated

Required: True
Position: 1
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

### -PlanName
Specifies the name of the website plan being deleted.
For example:

`-PlanName "Standard"`

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

### -RemoteSettings
{{Fill RemoteSettings Description}}

```yaml
Type: RemoteSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteMode
Specifies the site mode of the policy that this cmdlet removes.
Valid values are:

- Basic. Used with the Shared, Basic, and Standard plans. 
- Limited. Used with the Free plan.

For example:

`-SiteMode "Limited"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Limited, Dedicated

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SuppressRequestIdLine
{{Fill SuppressRequestIdLine Description}}

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

[New-WebSitesPolicy](xref:Websites/v1.0/New-WebSitesPolicy.md)

[Get-WebSitesPolicy](xref:Websites/v1.0/Get-WebSitesPolicy.md)

[Set-WebSitesPolicy](xref:Websites/v1.0/Set-WebSitesPolicy.md)


