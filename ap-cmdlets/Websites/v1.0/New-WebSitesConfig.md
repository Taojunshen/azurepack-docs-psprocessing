---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 1EB1CF72-C159-4800-B432-423C0FC56F41
online version: http://go.microsoft.com/fwlink/?LinkID=321243
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/New-WebSitesConfig.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/New-WebSitesConfig.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/New-WebSitesConfig.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-WebSitesConfig

## SYNOPSIS
Creates a website configuration type.

## SYNTAX

```
New-WebSitesConfig [-Type] <WebSitesConfigTypes> [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-WebSitesConfig** cmdlet creates a website configuration type.

## EXAMPLES

### Example 1: Create a configuration type
```
PS C:\> New-WebSitesConfig -Type "Global"
```

This command creates a global configuration type.

## PARAMETERS

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

### -Type
Specifies the configuration type.
Valid values are:

- AppHostConfig
- ConfigFile
- DefaultAppHostConfig
- RootWebConfig
- DefaultRootWebConfig
- RestAdmin
- Global
- Credential
- Metering
- Security
- SecurityKey
- CredentialCertificate

For example:

`-Type "ConfigFile"`

```yaml
Type: WebSitesConfigTypes
Parameter Sets: (All)
Aliases: 
Accepted values: AppHostConfig, ConfigFile, DefaultAppHostConfig, RootWebConfig, DefaultRootWebConfig, RestAdmin, Global, Credential, Metering, Security, SecurityKey, CentralCertificate

Required: True
Position: 0
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

[Get-WebSitesConfig](xref:Websites/v1.0/Get-WebSitesConfig.md)

[Set-WebSitesConfig](xref:Websites/v1.0/Set-WebSitesConfig.md)

[Remove-WebSitesConfig](xref:Websites/v1.0/Remove-WebSitesConfig.md)


