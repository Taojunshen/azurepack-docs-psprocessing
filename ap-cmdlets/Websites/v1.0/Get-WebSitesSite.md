---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: E2DFFF42-8E76-490F-BC44-02663AEF5D21
online version: http://go.microsoft.com/fwlink/?LinkID=321235
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSite.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSite.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSite.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesSite

## SYNOPSIS
Gets configuration information for a website site.

## SYNTAX

```
Get-WebSitesSite [[-Name] <String>] [[-SubscriptionId] <String>] [[-WebSpaceName] <String>] [-RawView]
 [-HostName <String>] [-Force] [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine]
 [-WorkerName <String>] [-OwnerName <String>] [-VirtualFarmName <String>] [-VirtualFarmOwnerName <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesSite** cmdlet returns configuration information for a website site.
When used without any parameters, **Get-WebSitesSite** returns information for all your website sites.
However, you can use parameters such as *Name*, *OwnerName*, or *WebSpaceName* to return a specified subset of your sites.
You can also use the *RawView* parameter to return detailed configuration information for each site.

## EXAMPLES

### Example 1: Return information about a site
```
PS C:\> Get-WebSitesSite -SiteName "Site01"
```

This command returns information about the site named Site01.

### Example 2: Return information about sites based on subscription and webspace
```
PS C:\> Get-WebSitesSite -SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce" -WebSpaceName "WebSpace01"
```

This command returns information for all sites with the subscription ID eede207d-d263-4212-ad32-fd29b5a1a6ceand the web space WebSpace01.

### Example 3: Return detailed information about sites
```
PS C:\> Get-WebSitesSite -RawView
```

This command returns detailed information for all your website sites.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
{{Fill Force Description}}

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

### -HostName
Specifies the hostname for the site being returned.
For example:

`-HostName "www.contoso.com"`

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

### -Name
Specifies the name of the site being returned.
For example:

`-Name "ContosoInternal"`

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

### -OwnerName
Specifies the name of a web site owner. 
For example:

`-OwnerName "PattiF"`

When this parameter is used *Get-WebSitesSite* returns information for sites owned by this user.

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

### -RawView
Indicates that detailed information is returned for a site.

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

### -SubscriptionId
Specifies the ID of a subscription.
For example:

`-SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce"`

When this parameter is used information is only returned for sites associated with the specified subscription ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

### -VirtualFarmName
Specifies the name of a virtual farm.
For example:

`-VirtualFarmName "ContosoVirtualFarm"`

When this parameter is used, information is returned for all the sites associated with the virtual farm.

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

### -VirtualFarmOwnerName
Specifies the owner of a virtual farm.
For example:

`-VirtualFarmOwnerName "PattiF"`

When this parameter is used, information is returned only for sites associated with virtual farms owned by the specified user.

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

### -WebSpaceName
Specifies a webspace. 
Default webspaces include:

- EastAsiaWebSpace
- EastUSWebSpace
- NorthCentralUSWebSpace
- NorthEuropeWebSpace
- WestEuropeWebsSpace
- WestUSWebSpace

For example:

`-WebSpaceName "EastUSWebSpace"`

When this parameter used, information is returned only for sites within the specified webspace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs. The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkerName
Specifies the name of a worker (workers perform background processing for websites).
For example:

`-WorkerName "ContosoWorker1"`

When this parameter is used, information is returned for all the sites associated with the specified worker.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-WebSitesSite](xref:Websites/v1.0/New-WebSitesSite.md)

[Set-WebSitesSite](xref:Websites/v1.0/Set-WebSitesSite.md)

[Restart-WebSitesSite](xref:Websites/v1.0/Restart-WebSitesSite.md)

[Remove-WebSitesSite](xref:Websites/v1.0/Remove-WebSitesSite.md)


