---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 4C714CC8-B9F8-4337-A1ED-ADB7882F2D6F
online version: http://go.microsoft.com/fwlink/?LinkID=321239
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesUser

## SYNOPSIS
Gets information about a website user.

## SYNTAX

```
Get-WebSitesUser [[-Name] <String>] [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesUser** cmdlet returns information about a website user.

## EXAMPLES

### Example 1: Get information about a user
```
PS C:\> Get-WebSitesUser -Name "User01"
```

This command returns information for the user User01.

## PARAMETERS

### -Name
Specifies the name of the website user whose information is being returned.
For example:

`-Name "PattiF"`

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

[New-WebSitesUser](xref:Websites/v1.0/New-WebSitesUser.md)

[Set-WebSitesUser](xref:Websites/v1.0/Set-WebSitesUser.md)

[Remove-WebSitesUser](xref:Websites/v1.0/Remove-WebSitesUser.md)


