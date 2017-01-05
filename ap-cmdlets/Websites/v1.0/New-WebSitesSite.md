---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 8AE320AF-9283-4BD0-AACC-A8CD6FC3CE5C
online version: http://go.microsoft.com/fwlink/?LinkID=321246
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/New-WebSitesSite.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/New-WebSitesSite.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/New-WebSitesSite.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-WebSitesSite

## SYNOPSIS
Creates a website site.

## SYNTAX

```
New-WebSitesSite [-SubscriptionId] <String> [-Name] <String> [-WebSpaceName <String>] [-HostNames <String[]>]
 [-SiteMode <String>] [-ComputeMode <ComputeModeOptions>] [-ServerFarm <String>] [-Tags <Hashtable>]
 [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-WebSitesSite** cmdlet creates a website site.

## EXAMPLES

### Example 1: Create a website site
```
PS C:\> New-WebSitesSite -Name "Site01" -SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce" -HostNames "Site01.Contoso.com" -SiteMode "Basic "-ComputeMode "Shared"
```

This command creates a website site named Site01.

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

Required: False
Position: Named
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

### -HostNames
Specifies one or more host names associated with the site.
For example:

`-HostName "contoso-internal.contoso.com"`

To specify multiple host names, separate the names by using commas:

`-HostName "contoso-internal.contoso.com", "employees.contos.com"`

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name for the site.
For example:

`-Name "ContosoInternal"`

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

### -ServerFarm
Specifies the server farm where the site is placed when switching to a reserved instance.
For example:

`-ServerFarm "DefaultServerFarm"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SiteMode
Specifies the site mode of the policy.
Valid values are:

- Basic. Used with the Shared, Basic, and Standard plans. 
- Limited. Used with the Free plan.

For example:

`-SiteMode "Basic"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Limited, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionId
Specifies the ID of the subscription to be associated with the site.
For example:

`-SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce"`

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

### -Tags
{{Fill Tags Description}}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebSpaceName
{{Fill WebSpaceName Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Get-WebSitesSite](xref:Websites/v1.0/Get-WebSitesSite.md)

[Set-WebSitesSite](xref:Websites/v1.0/Set-WebSitesSite.md)

[Restart-WebSitesSite](xref:Websites/v1.0/Restart-WebSitesSite.md)

[Remove-WebSitesSite](xref:Websites/v1.0/Remove-WebSitesSite.md)


