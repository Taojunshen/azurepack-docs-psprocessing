---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 05262BE6-2D24-4ECD-881E-8391C119E058
online version: http://go.microsoft.com/fwlink/?LinkID=321265
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Restart-WebSitesSite.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Restart-WebSitesSite.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Restart-WebSitesSite.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Restart-WebSitesSite

## SYNOPSIS
Restarts a website site.

## SYNTAX

```
Restart-WebSitesSite [-Name] <String> [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Restart-WebSitesSite** cmdlet restarts a website site.

## EXAMPLES

### Example 1: Restart a web site
```
PS C:\> Restart-WebSitesSite -Name "Site01"
```

This command restarts the website Site01.

## PARAMETERS

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

### -Name
Specifies the name of the website being restarted.
For example:

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

[New-WebSitesSite](xref:Websites/v1.0/New-WebSitesSite.md)

[Get-WebSitesSite](xref:Websites/v1.0/Get-WebSitesSite.md)

[Set-WebSitesSite](xref:Websites/v1.0/Set-WebSitesSite.md)

[Remove-WebSitesSite](xref:Websites/v1.0/Remove-WebSitesSite.md)


