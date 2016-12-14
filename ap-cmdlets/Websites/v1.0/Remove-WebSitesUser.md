---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 5BF8EB18-9910-4B5D-8CEF-01DB449F7C99
online version: http://go.microsoft.com/fwlink/?LinkID=321261
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-WebSitesUser

## SYNOPSIS
Removes a website user.

## SYNTAX

```
Remove-WebSitesUser [-Name] <String> [-Force] [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-WebSitesUser** cmdlet removes a website user.
If the specified user is the owner of one or more subscriptions those subscriptions must be removed (or the owner changed) before you can use **Remove-WebSitesUser** to delete the user account.

## EXAMPLES

### Example 1: Remove a user
```
PS C:\> Remove-WebSitesUser -Name "User01"
```

This command removes the website user User01.

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
Specifies the name of the website user being deleted.
For example:

`-Name "PattiF"`

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

[New-WebSitesUser](xref:Websites/v1.0/New-WebSitesUser.md)

[Get-WebSitesUser](xref:Websites/v1.0/Get-WebSitesUser.md)

[Remove-WebSitesSubscription](xref:Websites/v1.0/Remove-WebSitesSubscription.md)

[Set-WebSitesUser](xref:Websites/v1.0/Set-WebSitesUser.md)


