---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 21112410-3A0B-452B-94B4-ACBCA9172611
online version: http://go.microsoft.com/fwlink/?LinkID=321245
schema: 2.0.0
updated_at: 1/4/2017 6:14 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/New-WebSitesServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/New-WebSitesServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/34620cb46df1eb18f9e1c9a42639b53390ad35e3/AzurePack-cmdlets/Websites/v1.0/New-WebSitesServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-WebSitesServer

## SYNOPSIS
Creates a website server.

## SYNTAX

```
New-WebSitesServer [-Name] <String> [-ServerType] <ModifiableServerRole> [-Force]
 [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-WebSitesServer** cmdlet creates a website server.

## EXAMPLES

### Example 1: Create a server
```
PS C:\> New-WebSitesServer -Name "WSERVER01" -ServerType "WebWorker"
```

This command creates a new WebWorker server named WSERVER01.

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

### -Force
Forces the command to run without asking for user confirmation.

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

### -Name
Specifies the name of the server.
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

### -ServerType
Specifies the type of the server being created.
Valid values are:

- ManagementServer. Manages the website infrastructure. 
- LoadBalancer. Distributes and manages web traffic. 
- WebWorker. Hosts websites. 
- Publisher. Publishes content to file servers. 
- FileServer. Stores website content.

For example:

`-Type "FileServer"`

```yaml
Type: ModifiableServerRole
Parameter Sets: (All)
Aliases: 
Accepted values: ManagementServer, LoadBalancer, WebWorker, Publisher, FileServer

Required: True
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

[Get-WebSitesServer](xref:Websites/v1.0/Get-WebSitesServer.md)

[Set-WebSitesServer](xref:Websites/v1.0/Set-WebSitesServer.md)

[Test-WebSitesServer](xref:Websites/v1.0/Test-WebSitesServer.md)

[Restart-WebSitesServer](xref:Websites/v1.0/Restart-WebSitesServer.md)

[Repair-WebSitesServer](xref:Websites/v1.0/Repair-WebSitesServer.md)

[Remove-WebSitesServer](xref:Websites/v1.0/Remove-WebSitesServer.md)


