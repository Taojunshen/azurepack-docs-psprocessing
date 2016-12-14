---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 628F676F-2D72-4CB3-9E07-C2A56E36422A
online version: http://go.microsoft.com/fwlink/?LinkID=321251
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesApplication.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesApplication.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesApplication.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-WebSitesApplication

## SYNOPSIS
Removes a website web app.

## SYNTAX

```
Remove-WebSitesApplication [-SiteName] <String> [-ApplicationName] <String> [-WebSpaceName <String>]
 [-SubscriptionId <String>] [-PrefixMatch <Boolean>] [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-WebSitesApplication** cmdlet removes a website web app.

## EXAMPLES

### Example 1: Remove a web app
```
PS C:\> Remove-WebSitesApplication -SiteName "Site01" -ApplicationName "Application01"
```

This command removes the web app Application01 from the site Site01.

## PARAMETERS

### -ApplicationName
Specifies the name of the web app being removed.
For example:

`-ApplicationName "ContosoCalendar"`

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

### -PrefixMatch
{{Fill PrefixMatch Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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
Specifies the name of the site associated with the web app being removed.
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

[New-WebSitesApplication](xref:Websites/v1.0/New-WebSitesApplication.md)

[Get-WebSitesApplication](xref:Websites/v1.0/Get-WebSitesApplication.md)


