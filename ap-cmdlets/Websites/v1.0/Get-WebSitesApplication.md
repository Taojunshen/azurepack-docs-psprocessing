---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 052ABD1F-CF48-48C7-A214-B76FD7A359C2
online version: http://go.microsoft.com/fwlink/?LinkID=321228
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesApplication.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesApplication.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesApplication.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesApplication

## SYNOPSIS
Gets information about a website web app.

## SYNTAX

```
Get-WebSitesApplication [-SiteName] <String> [[-ApplicationName] <String>] [-WebSpaceName <String>]
 [-SubscriptionId <String>] [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesApplication** cmdlet returns information about website web apps.

## EXAMPLES

### Example 1: Get all the web apps for a web site
```
PS C:\> Get-WebSitesApplication -SiteName "Site01"
```

This command returns information for all the web apps associated with the website Site01.

## PARAMETERS

### -ApplicationName
Specifies the name of the web app for which information is being returned.
For example:

`-ApplicationName "ContosoCalendarApp"`

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

### -SiteName
Specifies the name of the site associated with the web app.
For example:

`-SiteName "ContosoInternal"`

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

### -SubscriptionId
{{Fill SubscriptionId Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-WebSitesApplication](xref:Websites/v1.0/New-WebSitesApplication.md)

[Remove-WebSitesApplication](xref:Websites/v1.0/Remove-WebSitesApplication.md)


