---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 0D5A0704-7D92-49D7-BB02-59DCB850A087
online version: http://go.microsoft.com/fwlink/?LinkID=321270
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesSite.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesSite.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesSite.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-WebSitesSite

## SYNOPSIS
Modifies configuration settings for a website site.

## SYNTAX

```
Set-WebSitesSite [-Name] <String> [-HostNames <String[]>] [-SiteMode <String>]
 [-ComputeMode <ComputeModeOptions>] [-ServerFarm <String>] [-AssignWorker <String>] [-UnassignWorker <String>]
 [-UnassignAllWorkers] [-SkipDnsRegistration] [-ForceDnsRegistration] [-TimeToLiveInSeconds]
 [-SkipCustomDomainVerification] [-Tags <Hashtable>] [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-WebSitesSite** cmdlet modifies the configuration settings for a website site.

## EXAMPLES

### Example 1: Remove all the workers from a site
```
PS C:\> Set-WebSitesSite -Name "Site01" -UnassignAllWorkers
```

This command removes all workers from site Site01.

### Example 2: Assign a worker to a site
```
PS C:\> Set-WebSitesSite -Name "Site01" -AssignWorker "WSERVER01"
```

This command assigns the worker WSERVER01 to the site Site01.

### Example 3: Remove a specific worker from a site
```
PS C:\> Set-WebSitesSite -Name "Site01" -UnassignWorker "WSERVER01"
```

This command removes the worker WSERVER01 from the site Site01.

## PARAMETERS

### -AssignWorker
Specifies a worker being assigned to the site.
For example:

`-AssignWorker "ContosoWorker"`

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

### -ComputeMode
Specifies the type of hosting environment that the web site runs in.
Valid values are:

- Shared. The web site runs in a shared/multi-tenant hosting environment. 

- Dedicated. The web site runs in its own dedicated hosting environment.

For example:

`-ComputeMode "Shared"`

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

### -ForceDnsRegistration
{{Fill ForceDnsRegistration Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HostNames
Specifies one or more hostnames associated with the site.
For example:

`-HostName "contoso-internal.contoso.com"`

To specify multiple hostnames, separate the names by using commas:

`HostName "contoso-internal.contoso.com", "employees.contos.com"`

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
Specifies the name of the site being modified For   example.

`-Name "ContosoInternal"`

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

### -ServerFarm
Specifies the server farm where the site is placed when switching to a reserved instances.
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
Specifies the site mode.
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

### -SkipCustomDomainVerification
{{Fill SkipCustomDomainVerification Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDnsRegistration
Indicates that DNS registration is not carried out.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -TimeToLiveInSeconds
{{Fill TimeToLiveInSeconds Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UnassignAllWorkers
Indicates that all workers are removed from the site.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UnassignWorker
Specifies a worker to remove from the site.
For example:

`-UnassignWorker "ContosoWorker"`

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

[New-WebSitesSite](xref:Websites/v1.0/New-WebSitesSite.md)

[Get-WebSitesSite](xref:Websites/v1.0/Get-WebSitesSite.md)

[Restart-WebSitesSite](xref:Websites/v1.0/Restart-WebSitesSite.md)

[Remove-WebSitesSite](xref:Websites/v1.0/Remove-WebSitesSite.md)


