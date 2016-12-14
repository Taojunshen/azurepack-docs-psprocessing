---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: C435C156-E82B-41C2-81E9-DD464FAFA168
online version: http://go.microsoft.com/fwlink/?LinkID=321250
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/New-WebSitesUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/New-WebSitesUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/New-WebSitesUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-WebSitesUser

## SYNOPSIS
Creates a website user.

## SYNTAX

```
New-WebSitesUser [-Name] <String> [[-PublishingUserName] <String>] [[-PublishingPassword] <String>]
 [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-WebSitesUser** cmdlet creates a website user.

## EXAMPLES

### Example 1: Create a user
```
PS C:\> New-WebSitesUser -Name "User01" -PublishingUserName "PubUser01" -PublishingPassword "PubPassWord01!"
```

This command creates a user that has the name User01.
In addition, the command specifies a publishing name and publishing password for the user.

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
Specifies the name for the user account.
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

### -PublishingPassword
Specifies the password for the PublishingUserName property.
PublishingUserName specifies the account name used for publishing website content.

For example:

`-PublishingPassword "p@ssw0rd"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublishingUserName
Specifies the user account name used when publishing website content.
For example:

`-PublishingUserName "PattiFPublishing"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

[Get-WebSitesUser](xref:Websites/v1.0/Get-WebSitesUser.md)

[Set-WebSitesUser](xref:Websites/v1.0/Set-WebSitesUser.md)

[Remove-WebSitesUser](xref:Websites/v1.0/Remove-WebSitesUser.md)


