---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: CE47F8DA-F696-4C47-AC10-95BD3783CB05
online version: http://go.microsoft.com/fwlink/?LinkID=321236
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesPolicy.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesPolicy.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesPolicy.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesPolicy

## SYNOPSIS
Gets policy information for a website.

## SYNTAX

```
Get-WebSitesPolicy [[-PlanName] <String>] [[-ComputeMode] <ComputeModeOptions>] [[-SiteMode] <String>]
 [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesPolicy** cmdlet returns policy information for a website.

## EXAMPLES

### Example 1: Get all website policies
```
PS C:\> Get-WebSitesPolicy
```

This command returns information about all your website policies.

## PARAMETERS

### -ComputeMode
Specifies the type of hosting environment that the web site runs in.
Valid values are:

- Shared. The web site runs in a shared/multi-tenant hosting environment. 

- Dedicated. The web site runs in its own dedicated hosting environment.

For example:

`-ComputeMode "Shared"`

If you use this parameter you must also use the *PlanName* parameter.

```yaml
Type: ComputeModeOptions
Parameter Sets: (All)
Aliases: 
Accepted values: Shared, Dedicated

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanName
Specifies the name of the plan associated with the policy.
For example:

`-PlanName "Shared"`

You must include this parameter if you use the *ComputeMode* and *SiteMode* parameters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
Specifies the site mode of the policy.
Valid values are:

- Basic. Used with the Shared, Basic, and Standard plans. 

- Limited. Used with the Free plan.

For example:

`-SiteMode "Basic"`

To use this parameter you must also specify a value for the *PlanName* parameter.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Limited, Dedicated

Required: False
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-WebSitesPolicy](xref:Websites/v1.0/New-WebSitesPolicy.md)

[Set-WebSitesPolicy](xref:Websites/v1.0/Set-WebSitesPolicy.md)

[Remove-WebSitesPolicy](xref:Websites/v1.0/Remove-WebSitesPolicy.md)


