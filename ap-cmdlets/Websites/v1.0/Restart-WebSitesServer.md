---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 663AC2F2-8535-4FAC-8F2A-9A610FD34B68
online version: http://go.microsoft.com/fwlink/?LinkID=321264
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Restart-WebSitesServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Restart-WebSitesServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Restart-WebSitesServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Restart-WebSitesServer

## SYNOPSIS
Restarts a website server.

## SYNTAX

```
Restart-WebSitesServer [-Name] <String> [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Restart-WebSitesServer** cmdlet restarts a website server.

## EXAMPLES

### Example 1: Restart a server
```
PS C:\> Restart-WebSitesServer -Name "WSERVER01"
```

This command restarts the server WSERVER01.

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
Specifies the name of the server being restarted.
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

[Repair-WebSitesServer](xref:Websites/v1.0/Repair-WebSitesServer.md)

[Remove-WebSitesServer](xref:Websites/v1.0/Remove-WebSitesServer.md)


