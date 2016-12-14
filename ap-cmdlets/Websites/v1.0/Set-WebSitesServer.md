---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: DA1159E5-A4B8-4AB2-85BC-03C5BE37F4BF
online version: http://go.microsoft.com/fwlink/?LinkID=321269
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-WebSitesServer

## SYNOPSIS
Enables or disables a website server.

## SYNTAX

```
Set-WebSitesServer [-Name] <String> [-Offline] <Boolean> [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-WebSitesServer** cmdlet enables or disables a website server.
If a server is disabled users will not be able to access websites associated with that server.

## EXAMPLES

### Example 1: Enable a server
```
PS C:\> Set-WebSitesServer -Name "WSERVER01" -Enabled
```

This command enables the server WSERVER01.

### Example 2: Disable a server
```
PS C:\> Set-WebSitesServer -Name "WSERVER01"
```

This command disables the server WSERVER01.
This is done by leaving out the *Enabled* parameter.

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
Specifies the name of the name of the server being enabled or disabled.
For example:

`-Name "ContosoServer"`

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

### -Offline
{{Fill Offline Description}}

```yaml
Type: Boolean
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

[New-WebSitesServer](xref:Websites/v1.0/New-WebSitesServer.md)

[Get-WebSitesServer](xref:Websites/v1.0/Get-WebSitesServer.md)

[Test-WebSitesServer](xref:Websites/v1.0/Test-WebSitesServer.md)

[Restart-WebSitesServer](xref:Websites/v1.0/Restart-WebSitesServer.md)

[Repair-WebSitesServer](xref:Websites/v1.0/Repair-WebSitesServer.md)

[Remove-WebSitesServer](xref:Websites/v1.0/Remove-WebSitesServer.md)


