---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: BF7E5622-C9CC-450D-A3BB-4998CEC10908
online version: http://go.microsoft.com/fwlink/?LinkID=321252
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesConfig.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesConfig.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesConfig.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-WebSitesConfig

## SYNOPSIS
Removes the specified website configuration type.

## SYNTAX

```
Remove-WebSitesConfig [-Type] <WebSitesConfigTypes> [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-WebSitesConfig** cmdlet removes the specified website configuration type.

## EXAMPLES

### Example 1: Remove a configuration type
```
PS C:\> Remove-WebSitesConfig -Type "AppHostConfig"
```

This command removes the AppHostConfig configuration type.

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

`-Type "SecurityKey"`

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

[New-WebSitesConfig](xref:Websites/v1.0/New-WebSitesConfig.md)

[Get-WebSitesConfig](xref:Websites/v1.0/Get-WebSitesConfig.md)

[Set-WebSitesConfig](xref:Websites/v1.0/Set-WebSitesConfig.md)


