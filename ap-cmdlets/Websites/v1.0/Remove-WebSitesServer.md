---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: F88FF268-35C6-4D59-A4DD-E2D1097011E4
online version: http://go.microsoft.com/fwlink/?LinkID=321256
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-WebSitesServer

## SYNOPSIS
Removes a website server.

## SYNTAX

```
Remove-WebSitesServer [-Name] <String> [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-WebSitesServer** cmdlet removes a website server.

## EXAMPLES

### Example 1: Remove a server
```
PS C:\> Remove-WebSitesServer -Name "WSERVER01"
```

This command removes the server WSERVER01.

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
Specifies the name of the server being removed.
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

[Set-WebSitesServer](xref:Websites/v1.0/Set-WebSitesServer.md)

[Test-WebSitesServer](xref:Websites/v1.0/Test-WebSitesServer.md)

[Restart-WebSitesServer](xref:Websites/v1.0/Restart-WebSitesServer.md)

[Repair-WebSitesServer](xref:Websites/v1.0/Repair-WebSitesServer.md)


